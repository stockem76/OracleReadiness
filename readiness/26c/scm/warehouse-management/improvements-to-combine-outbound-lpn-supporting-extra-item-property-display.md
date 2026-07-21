[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Improvements to Combine Outbound LPN supporting ‘Extra Item Property Display’

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50171.htm)

Combine Outbound LPN now displays additional item attributes during the combine process, giving warehouse users greater visibility into item details. This helps to quickly identify inventory, make informed decisions, and improve accuracy during container consolidation.

A new screen parameter **extra-item-property-disp** is introduced in the **Combine OBLPN**. Users can now display values such as item alternate code, item description, item barcode, season code, or other supported item fields.

**NOTE:**If the selected item property is not available, WMS does not display an extra value.

## ⚙️ Steps to Enable and Configure

1. Go to the Combine OBLPN screen parameters.
2. Set **extra-item-property-disp** to the item property users need to see.
3. Keep the value as Blank or None if users should only see the item code.
4. Confirm that the selected item property is populated in item setup.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*