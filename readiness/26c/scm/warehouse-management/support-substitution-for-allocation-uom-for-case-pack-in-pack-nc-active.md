[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Support Substitution for Allocation UOM for Case/Pack in Pack NC Active

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f49715.htm)

Mobile Pack NC Active now supports batch substitution when the allocation unit of measure is Cases or Packs. The transaction validates the substitute inventory before updating the allocation, supporting both full and partial substitutions while maintaining quantity and UOM integrity.

This enhancement helps pickers continue work when the originally allocated batch is unavailable by allowing controlled substitution of another eligible batch of the same item in the Mobile Pack NC Active flow.

**Key Considerations**

• • When a substitute batch is scanned, WMS validates that the substitute inventory Case or Pack quantity is an integral multiple of the allocated inventory Case or Pack quantity.
• WMS validates that the substitute inventory Case or Pack quantity does not exceed the allocated quantity being substituted.
• **If validation succeeds** - WMS updates the allocation for full or partial substitution and refreshes the mobile screen with the correct quantity and Case or Pack UOM conversion for the new inventory.
• **If validation fails** -  the picker receives an error indicating whether the scanned inventory quantity is not an integral multiple or exceeds the allocated quantity.

## ⚙️ Steps to Enable and Configure

1. 1. Use this capability in the **Mobile Pack NC Active** flow. Ensure item, batch, and Case/Pack UOM conversion data is maintained accurately so substitution validations can be applied correctly.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*