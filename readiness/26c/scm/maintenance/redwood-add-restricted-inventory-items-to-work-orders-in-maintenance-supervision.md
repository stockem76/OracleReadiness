[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Maintenance](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/maintenance.md)

# Redwood: Add Restricted Inventory Items to Work Orders in Maintenance Supervision

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/maint26c/26C-maintenance-wn-f46403.htm)

Items can typically be received into or issued from any valid subinventory within an inventory organization. Restricted items, however, can only be transacted within the specific subinventories and locators assigned to the item by enabling the **Restrict Subinventories** and **Restrict Locators** item attributes.

In previous updates, restricted items weren't considered during subinventory and locator selection in maintenance pages. In this update, maintenance pages support restricted items by validating and limiting subinventory and locator selections based on item restrictions. Restricted subinventory and locator values are no longer defaulted and are limited to only valid values for the item in context.

The following maintenance pages now support restricted items:

• **Maintenance Supervision**
• **Work Order Materials** tab for supply subinventory and locator selection
• **Work Order Details** tab for completion subinventory and locator selection for inventory completion work orders 
    • For transform work orders, restrictions are based on the target item instead of the work order item.
• **My Maintenance Work**
• **Material issue and return** drawer on the **Report Work**page
• **Complete Work Order** page for completion subinventory and locator selection for inventory completion work orders

This feature helps organizations enforce inventory controls for restricted items during maintenance execution and material transactions.

Improve inventory control and transaction accuracy by ensuring subinventory usage aligns with item restrictions. Reduce errors and maintain consistent, compliant material handling across maintenance processes.

## ⚙️ Steps to Enable and Configure

To configure restricted items for maintenance transactions:

1. Navigate to the item definition or organization item setup.
2. Enable the **Restrict Subinventories** attribute for the item.
3. Assign valid subinventories to the item.
4. Optionally, enable the **Restrict Locators** attribute and assign valid locators.

Use the Redwood **Configure Subinventories** pages to create subinventories and locators and associate items with valid subinventories and locators.

---
*Oracle Cloud Readiness · 26C · SCM · Maintenance*