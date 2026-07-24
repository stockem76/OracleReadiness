[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Manufacturing](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/manufacturing.md)

# Allow Over-Issue When Picking Materials for Work Orders

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/mfg26c/26C-mfg-wn-f44521.htm)

Warehouse operators can now issue more than the requested component quantity during work order picking when shop floor handling conditions require it. This enhancement supports situations where materials are picked in full cases, reels, packs, pallets, or other packaging units and the exact required quantity cannot be efficiently split during picking. When enabled for the inventory organization, the picking flow allows the actual picked quantity to be issued to the work order instead of forcing operators to use a separate overpick-and-move workaround. This improves alignment between system transactions and real-world material handling on the factory floor.

Picking and issuing quantities greater than the work order requirement is applicable for discrete, process, and maintenance manufacturing work orders when enabled at the organization level. Overissued quantities are recorded and tracked against the work order to provide clear traceability and support reconciliation when unused material is returned after the production or maintenance activity.

Work Order Operation Item

Pick More than the Required Quantity

Overpicked Component

Overissued Component in Work Order Operation

This feature increases warehouse efficiency and provides the following benefits:

• Reduces manual workarounds when materials must be picked in fixed packaging quantities.
• Improves inventory accuracy and traceability by recording the actual overissued quantity against the work order.
• Supports smoother shop floor execution and fewer delays in material staging and issue.
• Simplifies reconciliation and surplus material management after completing production or maintenance.

*Here's the demo of these capabilities:*

## ⚙️ Steps to Enable and Configure

1.    In the Setup and Maintenance work area, search for the 'Manage Inventory Organizations' task.

  2.    In the **Item Sourcing Details** tab, enable the **Overpicking for work orders enabled** checkbox and save the changes.

Enable Overpicking for the Inventory Organization

## 💡 Tips and Considerations

• Overissue control isn't available for contract manufacturing or Warehouse Management System (WMS)-enabled organizations.
• Overissue is controlled only at the organization level and can't be managed at the item, component, or work center level.
• When the parameter is enabled, pick confirm doesn't apply a tolerance limit to the overissued quantity.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains the following privileges can use this feature:

• WIP_MANAGE_WORK_ORDER_COMPONENT_PICKING_PRIV (Pick Components for Work Orders)
• INV_PRINT_MOVEMENT_REQUEST_PICK_SLIP_REPORT_PRIV (Print Movement Request Pick Slip Report)

These privileges were available prior to this update.

## 📚 Key Resources

• Watch the 26D feature 'Allow Over-Issue When Picking Materials for Work Orders' demo.
• Oracle Fusion Cloud SCM: Refer to the Using Manufacturing guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Refer to the Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Manufacturing*