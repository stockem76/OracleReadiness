[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Honor Expiry Date Range Rules for Direct Allocation

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50401.htm)

Direct Allocation now supports expiry date validation during allocation. A new screen parameter, **Expiry Date Range Rule**, lets customers define which expiry date range rule WMS applies when users allocate inventory from a scanned LPN or pallet to an order.

• A new mobile screen parameter: Expiry Date Range Rule has been introduced. 
• If the parameter is blank, WMS continues the existing Direct Allocation flow.
• If the parameter is configured, WMS allocates only inventory that falls within the configured expiry date range.
• If no inventory in the scanned LPN or pallet meets the rule, allocation fails, and WMS displays a warning.
• If inventory meets the rule, WMS allocates the inventory and continues to pack.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*