[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Improvements to Get API Support

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50172.htm)

**GET APIS FOR MOVEMENT REQUEST STATUS AND CROSS-REFERENCE DATA**

WMS now supports GET API access for the following movement request status and detail mapping entities.

• movement_request_status
• movement_request_dtl_status
• movement_request_dtl_order_dtl_xref

APIs support paginated retrieval and single-record retrieval by ID.

**GET API FOR IN-TRANSIT INVENTORY**

WMS now supports GET API access for in_transit_inventory. Users can retrieve in-transit inventory records through LGFAPI.

**GET API FOR PALLET HISTORY**

WMS now supports GET API access for **pallet_history**.

• Customers can retrieve pallet activity and movement history through LGFAPI.
• The API supports paginated retrieval and single-record retrieval by ID.

**GET API FOR STAGE LOCATION CONFIGURATION**

WMS now supports GET API access for **stage_location_config**.

• Customers can retrieve stage location configuration records through LGFAPI.
• The API supports paginated retrieval and single-record retrieval by ID.

## ⚙️ Steps to Enable and Configure

Review the REST service definition in the REST API guides to leverage (available from the Oracle Help Center > *your apps service area of interest* > APIs & Schema). If you are new to Oracle's REST services you may want to begin with the Quick Start section.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*