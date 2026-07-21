[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# Export API - Delete Supported For Tender Collab Tables

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f49639.htm)

This feature extends the tables where deletes are provided in the Export API to include the set of tables below.

TENDER_COLLAB_SERVPROV

                 TENDER_COLLABORATION

                 TENDER_COLLABORATION_STATUS

                 SERVPROV_TENDER_COMMENT

                 SERVPROV_TENDER_REFNUM

                 ACCESSORIAL_CODE

                 BULK_PLAN

                 CORPORATION_PROFILE_DETAIL

                 EQUIPMENT_GROUP_PROFILE_D

                 RATE_GEO_ACCESSORIAL

                 RATE_GEO_COST_GROUP

                 RATE_ZONE_PROFILE_D

                 REGION_DETAIL

                 RO_SPECIAL_SERVICE  

                 SS_STATUS_HISTORY

                 SS_STATUS_HISTORY_EVENT_GROUP

                 X_LANE

**Business Benefit:**This feature simplifies the synchronization of deleted Tender Collaboration records from OTM to your external data lake.

For tender messages sent to service providers, transactional deletes matter because they let the lake reflect real business state, not just what was once emitted. That helps in a few ways:

• **Correctness of downstream analytics.** If a tender message is canceled, retracted, or invalidated in the source system, downstream reports and models should not keep treating it as active.
• **Cleaner operational reporting.** Metrics like tender volume, acceptance rate, response time, and provider engagement stay accurate when deleted or voided records are removed or marked consistently.
• **Reduced duplicate and stale data.** Transportation workflows often produce retries, amendments, and reversals. Delete propagation prevents old versions from accumulating and distorting results.
• **Better compliance and retention control.** If a tender message must be removed for policy, contractual, or privacy reasons, the lake can honor that action instead of retaining data indefinitely by accident.
• **Trust in the lake as a governed copy.** Users are more likely to rely on the corporate data lake when it behaves like a managed mirror of source-system truth, including deletions.
• **Safer downstream automation.** Forecasting, SLA monitoring, carrier scorecards, and exception detection all work better when they are not trained or triggered by records that should no longer exist.

## ⚙️ Steps to Enable and Configure

The Export API delete for the supported Tender Collab Tables follows the same process used for other delete transactions.

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*