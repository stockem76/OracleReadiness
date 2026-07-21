[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Manufacturing](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/manufacturing.md)

# Manage and Execute Flow Schedules in Organizations Enabled for Inventory Tracking by COO or Integrated with WMS

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/mfg26c/26C-mfg-wn-f44542.htm)

Lean manufacturers need to synchronize material flows with integrated warehouse management and origin traceability, ensuring uninterrupted production while maintaining compliance. With this feature, you can manage and execute flow schedules in organizations that are enabled for inventory tracking by Country of Origin or integrated with the Warehouse Management System (WMS).

**WMS Integration:** This feature delivers services and core application enhancements to support integrations of flow schedule completion transactions reported in Oracle Fusion Cloud Manufacturing to an external warehouse management system or Oracle Fusion Cloud Warehouse Management. You can also conditionally enter a Packing Unit (also known as LPN in WMS) while reporting a flow schedule completion transaction.

**Country of Origin:**You can enter country of origin while reporting flow schedule completions as part of the product details and backflush country-of-origin specific material while reporting flow schedule completions.

Enter Packing Unit and Country of Origin While Reporting Flow Schedule Completion

Once reported, you can schedule the **Generate Manufacturing and Maintenance Transactions for External Systems** process to transfer the transactions related to flow schedule completions to Oracle WMS. After the scheduled process completes, you can review the status of the transactions using the Review Completed Transactions page in Inventory Management. The **Integration Status** column shows if the transactions were interfaced to WMS, and the **External Packing Unit** field captures the packing unit provided while reporting the flow schedule completion transaction. The transactions are interfaced to WMS using the pre-built **Oracle INV WMS Work Order Direct Transactions** integration that sends transactions from Oracle Fusion Cloud Inventory Management to Oracle WMS using Oracle Integration Cloud.

Review Integration Status of Completed Transactions

The flow completion transactions that were interfaced to WMS can be reviewed in Oracle WMS in the **From Manufacturing Transaction Header** page.

Review Flow Schedule Completion Transactions in WMS

This feature improves efficiency and inventory accuracy related to flow schedule execution through seamless integration between manufacturing and warehouse management systems. It reduces manual effort, minimizes transaction errors, accelerates material movement, and lowers integration effort through pre-delivered OIC-based mappings. It enables flow manufacturers to accurately capture and monitor inventory by country of origin, supporting compliance reporting for import and export documentation.

*Here's the demo of these capabilities:*

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Manufacturing and Supply Chain Materials Management*

1. Enable the "**Integrate Manufacturing and Maintenance Direct Work Order Transactions with Your Warehouse Management System"** Opt In feature.

Enable Feature Opt In

2. Enable the "**Enable inventory tracking by country of origin**" and "**Integrate manufacturing and maintenance with WMS**" plant parameters.

Enable Plant Parameters for COO Tracking and WMS Integration

3. Enable the "**Use subinventory for manufacturing and maintenance integration with WMS**" attribute for WMS integration. Optionally enable the " **Use packing unit for product completions and returns**" attribute if packing unit (also known as LPN in WMS) is required for product completion.

Enable Subinventory Attributes for WMS Integration

## 💡 Tips and Considerations

• Refer to the 24D What's New: Integrate Manufacturing and Maintenance Direct Work Order Transactions with Your Warehouse Management System.
• Refer to the 25A What's New: Manage Flow Schedules for Manufacturing Execution on a Production Line and Execute Flow Schedules on a Production Line.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these duty roles and privileges can access this feature:

• **Manufacturing Privilege:**
• Execute Flow Schedules (WIP_EXECUTE_FLOW_SCHEDULES_PRIV)
• **Inventory Duty Role and Privilege:**
• Inventory Transaction Management Duty (ORA_INV_INVENTORY_TRANSACTION_MANAGEMENT_DUTY)
• Generate Manufacturing and Maintenance Transaction Data for External Systems (INV_INTERFACE_WO_TRANSACTIONS_TO_EXT_SYS_PRIV)

The duty role and privileges were available prior to this update.

## 📚 Key Resources

• Watch the Manage and Execute Flow Schedules in Organizations Enabled for Inventory Tracking by COO or Integrated with WMS demo.
• Oracle Fusion Cloud SCM: Refer to the Using Manufacturing guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Refer to the Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.
• Oracle Warehouse Management Cloud: WMS REST API Guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Manufacturing*