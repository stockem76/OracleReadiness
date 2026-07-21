[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Honor Expiry Date Range Rules for Cross Dock Pick And Allocate

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50402.htm)

Pick and Allocate now validates picked inventory against an Expiry Date Range rule before allocation. A new mobile screen parameter**, Expiry Date Range Rule,** controls this behaviour. WMS uses the configured rule to determine whether the scanned inventory can be allocated to the order.

• A new screen parameter: Expiry Date Range Rule has been introduced and is applicable for both active, reserve locations, user-directed and system-directed Pick and Allocate flows. 
• If the parameter is blank, WMS continues the existing Pick and Allocate flow.
• If the parameter is configured, WMS allows allocation only when the inventory expiry date is within the configured range.
• If the inventory is outside the allowed range, WMS displays “Inventory is not within the configured expiry date range.”

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*