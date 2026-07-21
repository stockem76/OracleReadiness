[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Cancel Picking Allocations only for a Replenishment with Picking Wave

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f49718.htm)

Warehouse operators often manage a high volume of order changes, including order cancellations, while simultaneously running both picking and replenishment waves. In some situations, customer orders tied to a picking wave may be canceled, but the associated replenishment activity is still required to maintain inventory levels in the warehouse.

To support this operational need, a new **Cancel Picking Allocations Only** action is now available in the **Wave Inquiry** screen for Replenishment with Picking Waves. This allows you to cancel only the picking allocations associated with a wave while preserving the replenishment allocations.

**Key Considerations**

• Available only for Replenishment with Picking Waves
• Cancels only the picking allocations for the selected wave
• Retains all existing replenishment allocations
• Regenerates the Wave Pick Info output file, if configured
• Does not regenerate the Replenishment Wave Pick Info file, since replenishment allocations remain unchanged

**Automatically handles all related updates, including:**

• Tasks
• Orders
• Inventory History Transactions (IHTs)
• Other associated picking allocation records

When the action is selected, the system displays a confirmation message prompting the user to proceed with the cancellation of picking allocations only.

**NOTE:**  The action is enabled only when the selected wave is a Replenishment with Picking Wave and picking activity for the wave has not yet started.

## ⚙️ Steps to Enable and Configure

**Steps to Enable**

To use this feature:

1. Ensure the user has the same permissions required for the **Undo Wave** action.
2. Verify the facility parameter **UNDO_WAVE_EVEN_AFTER_PICKING** is configured appropriately for your operational policies.
3. Optionally configure the Wave Pick Info output file generation if outbound wave files are used in your environment.

**NOTE**:  If picking has already started, the action remains unavailable, even if replenishment processing is still in progress.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*