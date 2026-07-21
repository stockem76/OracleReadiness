[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Support task_nbr parameter in Pick Confirm API

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50173.htm)

The Pick Confirm API now supports **task_nbr** as an optional allocation filter. Users can pass task_nbr in the API payload.

WMS uses the task number with other filters to find the correct allocation.

• If no matching open allocation exists, WMS returns an error.
• If task_nbr is not provided, existing API behavior remains unchanged.

**NOTE****:**The From MHE Pick Confirmation UI also includes Task Number in the grid and search.

## ⚙️ Steps to Enable and Configure

Review the REST service definition in the REST API guides to leverage (available from the Oracle Help Center > *your apps service area of interest* > APIs & Schema). If you are new to Oracle's REST services you may want to begin with the Quick Start section.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*