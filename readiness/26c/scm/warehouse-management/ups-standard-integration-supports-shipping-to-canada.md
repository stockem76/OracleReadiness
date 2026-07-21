[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# UPS Standard Integration Supports Shipping to Canada

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50178.htm)

UPS Standard integration now supports international shipping to Canada by sending invoice line total information.

• WMS maps Invoice Line Total for UPS Standard shipments to Canada.
• WMS calculates invoice line total using item unit cost and quantity in the OBLPN.
• This supports tracking number generation for eligible UPS Standard shipments to Canada.
• Item unit cost must be greater than zero for the invoice line total to be valid.
• If item unit cost is zero, manifesting may fail because UPS requires a monetary value greater than zero.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 📚 Key Resources

See the Parcel Carrier Integration Guide on the Release 26C Documentation page.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*