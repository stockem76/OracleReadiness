[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Cancel Picking Allocations Only from Wave Inquiry

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50174.htm)

Wave Inquiry now supports canceling picking allocations while retaining replenishment allocations for replenishment with picking waves.

• A new action button “**Cancel Picking Allocs Only**” is introduced. The action applies only to replenishment with picking waves.
• WMS cancels only the picking allocations and keeps replenishment allocations unchanged.
• The action uses the same permission model as Undo Wave.
• WMS continues to honour the UNDO_WAVE_EVEN_AFTER_PICKING facility parameter.
• If picking has already started and the facility setup does not allow undo after picking, the action remains unavailable.

## ⚙️ Steps to Enable and Configure

1. Review user permissions for Undo Wave and grant the required permission for performing cancel picking allocations.
2. Review the UNDO_WAVE_EVEN_AFTER_PICKING facility parameter.
3. Use the new action from Wave Inquiry for replenishment with picking waves.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*