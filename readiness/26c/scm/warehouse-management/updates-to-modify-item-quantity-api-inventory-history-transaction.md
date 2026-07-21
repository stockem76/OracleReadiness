[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Updates to Modify Item Quantity API Inventory History Transaction

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50164.htm)

The Modify Item Quantity API now supports inventory history updates for serial-tracked items when users pass an adjustment quantity.

Supported API flows include:

• `POST .../entity/iblpn/modify_item_qty`
• `POST .../entity/iblpn/{id}/modify_item_qty`

Users must give the adjust qty and perform modify Item qty. Upon adjusting the quantity, the system updates the inventory and writes IHT records only for the adjusted quantity and not for actual qty.

**NOTE:** If users pass a negative adjustment_qty in the API request for a serial-tracked item, WMS updates the inventory and records inventory history only for the adjusted quantity and the related serial numbers.

## ⚙️ Steps to Enable and Configure

Review the REST service definition in the REST API guides to leverage (available from the Oracle Help Center > *your apps service area of interest* > APIs & Schema). If you are new to Oracle's REST services you may want to begin with the Quick Start section.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*