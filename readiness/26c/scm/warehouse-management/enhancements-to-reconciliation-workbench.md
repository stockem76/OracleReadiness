[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Enhancements to Reconciliation Workbench

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50167.htm)

WMS now includes core product changes to support full and partial ERP inventory synchronization for inventory reconciliation.

**INTRODUCING NEW PARAMETER IN GENERATE INVENTORY BALANCE SNAPSHOT SCHEDULE JOB**

The Generate Inventory Balance Snapshot scheduled job now includes a new **partial_sync_flg** parameter. Users can use this parameter to identify whether the run represents a full sync or a partial sync.

• A **blank**or **no**value is treated as full sync.
• A **yes**value identifies the run as partial sync.
• **NOTE:**
• If the partial sync is set to **Yes** and there is no prior successful run existing, then WMS treats the run as a full inventory sync.
• Existing prebuilt integration to fetch ERP on-hands is NOT impacted and will be handled in subsequent releases. Users can still use this flag in case of building a custom integration fetch the ERP on-hand.

The inventory balance snapshot includes a unique Run_nbr that identifies each synchronization cycle. ERP systems use this run number when sending inventory balance data so that Oracle Warehouse Management can accurately compare inventory balances between the two systems.

Oracle Warehouse Management provides the **Inventory Summary Run Number** output interface to make the run number available to non-Fusion ERP systems. In 26C, the application generates this output interface only for non-Oracle / custom integration, helping reduce unnecessary interface generation and processing.

**INVENTORY SUMMARY RUN NUMBER OUTPUT INTERFACE TRIGGER**

The scheduled job parameter **generate_erp_inv_summary_flg** is now renamed to **generate_erp_inv_summary_trigger_type**. This parameter supports following values:

• no or blank: WMS generates the WMS on-hand snapshot only.
• prebuilt: WMS generates the WMS on-hand snapshot and triggers the prebuilt integration for ERP on-hand balance.
• non_oracle: WMS generates the WMS on-hand snapshot and creates the Inventory Summary Run Number output interface.

**NOTE:** By default, the **generate_erp_inv_summary_trigger_type** is set to blank. All the existing configs where the **generate_erp_inv_summary_flg** is set to yes will be updated to **generate_erp_inv_summary_trigger_type** as prebuilt post 26C migration.

The Inventory Summary Run Number output interface is now generated only when **generate_erp_inv_summary_trigger_type** is set to **non_oracle**. For non-Oracle ERP integrations, the output interface now includes the generated run number and the partial sync flag, so the external host system can return the same sync mode with the ERP Inventory Summary payload.

**Current state**

Parameter | Value | Behaviour | Outcome
generate_erp_inv_summary_flg | no/blank | Generates WMS on hand | Always generates Run number o/p interface
generate_erp_inv_summary_flg | yes | Generates WMS on hand+ Triggers prebuilt for ERP on hand | Always generates Run number o/p interface

**Future state**

Parameter | Value | Behaviour | Outcome
generate_erp_inv_summary_trigger_type | no/blank | Generates WMS on hand | Run number o/p interface not generated
generate_erp_inv_summary_trigger_type | prebuilt | Generates WMS on hand +Triggers prebuilt for ERP on hand | Run number o/p interface not generated
generate_erp_inv_summary_trigger_type | non_oracle | Generates WMS on hand | Run number o/p interface generated

For more information on the payload, please refer to the Interface Formats.

**ERP INVENTORY SUMMARY INTERFACE SUPPORTS CREATEUPDATE ACTION WITH PARTIAL SYNC FLAG**

The ERP Inventory Summary interface now supports partial sync processing through the partial_sync_flg field. When the flag is Yes, WMS Creates inventory records that do not already exist and Updates existing records without creating duplicates. When the flag is no or blank, WMS continues to use the existing full sync behaviour.

**NOTE:** Though these fields are available in the ERP Inventory Summary Interface, they are NOT available for the current prebuilt integration. Users can still use these flags where the CREATEUPDATE action for custom integrations.

**ERP INVENTORY SUMMARY DATA RETENTION AND PURGE**

WMS now purges older ERP inventory summary data to reduce storage growth.

• For partial sync processing, WMS maintains a **single run**.
• For full sync processing, WMS retains a maximum of the latest **two** **sets** of ERP inventory summary runs. WMS inventory summary and discrepancy history remain available according to existing behaviour.

**GET API FOR WMS ERP INVENTORY DISCREPANCY HEADER**

WMS also provides a new GET API (WMS_ERP_INV_DISCREPANCY_HDR) support for the discrepancy header so integrations can retrieve the run context, ERP job reference number, partial sync flag, status, and related details.

`GET... wms/lgfapi/v10/entity/wms_erp_inv_discrepancy_hdr`

**ERP ON-HAND PROCESSING TIMEOUT**

WMS adds guardrails to the Generate Inventory Balance Snapshot scheduled job. If ERP on-hand extraction or inventory discrepancy computation is still in progress for the same company and facility, WMS prevents another Generate Inventory Balance Snapshot scheduled job from starting for that same company and facility. Users can still run the job for other eligible company and facility combinations.

A new company parameter, **erp_on_hand_processing_timeout** is introduced where it defines the maximum duration, in hours, that WMS waits for ERP on-hand processing after the Generate Inventory Balance Snapshot job starts.

• If the parameter is blank or incorrectly configured, WMS uses 24 hours as the default.
• When ERP on-hand processing exceeds the configured timeout, WMS marks the stale discrepancy run as failed and allows users to start a new snapshot job for the same company and facility.

**POST API TO RELEASE GUARDRAIL AFTER ERP JOB FAILURE**

WMS also provides a POST API to release the guardrail when the ERP job fails. This allows the integration to notify WMS that the ERP on-hand fetch failed, so users do not need to wait for the timeout period before running the snapshot job again.

**NOTE:** Currently, this is not applicable to the current prebuilt integration. Users can still use this call to build a customer integration to fetch the ERP on-hands.

`POST .../wms/lgfapi/v10/entity/wms_erp_inv_discrepancy_hdr/set_failed`

Please refer to WMS REST API for more information.

## ⚙️ Steps to Enable and Configure

1. Configure the Generate Inventory Balance Snapshot scheduled job.

• Set partial_sync_flg based on the type of inventory synchronization you want to run:
• Blank or no: Runs a full sync.
• yes: Runs a partial sync.

If partial sync is selected and WMS does not find a prior successful run, WMS processes the run as a full sync.

1. Configure the ERP inventory summary trigger type.

• Set generate_erp_inv_summary_trigger_type based on your integration type:
• Blank or no: Generate the WMS on-hand snapshot only.
• prebuilt: Generate the WMS on-hand snapshot and trigger the ERP on-hand prebuilt integration.
• non_oracle: Generate the WMS on-hand snapshot and create the Inventory Summary Run Number output interface.

1. For non-Oracle ERP integrations, consume the Inventory Summary Run Number output interface.

• When generate_erp_inv_summary_trigger_type is set to non_oracle, WMS generates the Inventory Summary Run Number output interface.
• Use the generated run_nbr and partial_sync_flag from this output interface when sending ERP inventory summary data back to WMS.

1. Send the partial sync flag with ERP inventory payloads.

• Include partial_sync_flg in the ERP Inventory Summary interface payload.

1. • No/ blank: WMS processes the payload using full sync behavior.
• Yes: WMS creates missing inventory records and updates existing records without creating duplicates.
2. Send the partial sync flag, if serial-controlled inventory is used.

• Include partial_sync_flg in the interface payload.

• • No/ blank: WMS uses existing full sync behavior.
• true: WMS creates missing serial records and updates existing serial records without creating duplicates.

**NOTE:** Do not send both run_nbr and erp_job_reference_nbr in the same payload.

1. Configure the ERP on-hand processing timeout.

• Set the company parameter erp_on_hand_processing_timeout to define how many hours WMS should wait for ERP on-hand processing before releasing the snapshot job guardrail.
• If the parameter is blank or incorrectly configured, WMS uses 24 hours as the default.

1. Use the discrepancy header APIs for integration status updates, if applicable.

• Use the GET API for wms_erp_inv_discrepancy_hdr to retrieve run context details such as run number, ERP job reference number, partial sync flag, and status.
• If the ERP job fails, call the POST API to mark the ERP on-hand fetch as failed so WMS can release the guardrail for the same company and facility.

**Important Note:**For 26C, these steps enable the WMS core product changes. The prebuilt integration continues to process ERP inventory as a full sync until the related integration enhancement is delivered in a future release.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*