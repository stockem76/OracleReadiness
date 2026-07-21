[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Locate Received LPNs During Receive Entire Shipment

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50595.htm)

Warehouse operations can now receive an entire shipment and assign the received LPNs to a location in the same flow. This reduces the time between receiving and putaway, helps keep inventory tied to the correct shipment and purchase order information, and lowers the risk of inventory discrepancies caused by LPN split or combine activity after receiving. This enhancement also helps customers make received inventory available for downstream inventory and allocation processes sooner, while applying the same location, capacity, and inventory validations used in receiving flows.

Oracle WMS Cloud now supports location assignment as part of the **Receive Entire Shipment** process from both the API and the IB Shipment UI.

For API-based receiving, the **Receive Entire Shipment API** now supports the **location_barcode** option. When users pass a valid location barcode, the system receives the shipment and attempts to locate the received LPNs to the specified location.

For UI-based receiving, the IB Shipment UI includes a new screen parameter, prompt-location, with the following behavior:

• No or blank: The system keeps the existing Receive Entire Shipment behavior and does not prompt for a location.
• Yes: The system displays a mandatory location prompt after receipt confirmation. Users can scan, enter, search, and select a location.

Users can select Reserve, Drop, or Active locations.

The system updates the received LPNs and shipment details based on the selected location:

• LPNs moved to Reserve or Drop locations are set to **Located**.
• LPNs moved to Active locations are set to **Consumed**.
• The system updates the LPN location and status in the IBLPN UI and IB Shipment Detail.
• The system writes inventory history transactions for the location movement, including IHT-51 for Reserve or Drop locations and IHT-2/IHT-4 for Active locations.

As part of this enhancement, the system also validates for Invalid location barcode, Location type, Item assignment type, Allow Multi-SKU rules, Maximum units, Maximum LPNs, Capacity checks for weight, volume, and dimensions, Restricted batch and attribute rules. If the location barcode is invalid, the system returns the error **Invalid Location Barcode**.

For asynchronous processing, the system check’s location barcode, location type, maximum units, maximum LPNs, and Multi-SKU rules before receiving starts. It checks restricted batch or attribute rules and weight, volume, and dimension capacity after receiving starts for each LPN. Depending on these validations, some LPNs may be located while others may remain received.

• Additionally, for cartonized shipments with **expense_destination_flg = Y**, LPNs move to **Consumed** after receiving.
• For cartonized shipments with **expense_destination_flg = N**, LPNs move to **Received**, and the system locates only the received LPNs.
• When **consider-mark-for-qc-flg** is enabled, the system marks applicable LPNs for QC and locates only the LPNs that are not marked for QC.
• If a shipment already contains received or located LPNs, the system locates only the LPNs received in the current Receive Entire Shipment flow and excludes LPNs that are already located.

## ⚙️ Steps to Enable and Configure

1. Go to the **IB Shipment UI** screen configuration.
2. Enable the new screen parameter: **prompt-location = Yes**
3. Save the screen configuration.
4. When users perform **Receive Entire Shipment** from the IB Shipment UI, the system displays a mandatory location prompt after receipt confirmation.
5. Users can scan, enter, search, or select a valid **Reserve**, **Drop**, or **Active** location.
6. For API-based receiving, pass the new location option in the Receive Entire Shipment API request. Refer WMS REST API guide for more information.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*