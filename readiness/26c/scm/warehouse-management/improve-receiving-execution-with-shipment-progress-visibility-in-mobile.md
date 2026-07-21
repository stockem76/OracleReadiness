[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Improve Receiving Execution with Shipment Progress Visibility in Mobile

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50590.htm)

Warehouse operators and supervisors can now view real-time shipment receiving progress directly within Mobile receiving transactions. The enhancement provides shipment-level visibility into key receiving metrics, allowing users to monitor receiving progress without navigating to other screens or running reports.

The receiving transaction now displays operational KPIs such as percentage of units received, units received, LPNs received, and pallets received for the shipment. These metrics update dynamically throughout the receiving process, enabling users to quickly verify shipment status, identify exceptions, and better coordinate downstream warehouse activities. This reduces time spent navigating multiple screens or running reports, improves receiving accuracy, and helps shorten dock-to-stock cycle times while improving overall warehouse productivity.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## Display the Count of LPNs in the Pallet

During palletized receiving, the **Mobile Receive by Shipment** (rf.inbound.cwrfrecvlpnshpmt) and **Receive by Load** (rf.inbound.cwrfrecvlpnload) transactions now display the number of LPNs currently associated with the pallet being received. The count is shown after scanning the pallet and updates as LPNs are received, providing users with real-time visibility into pallet receiving progress. If inventory has already been received against the shipment, the existing LPN count is displayed when the pallet is scanned.

This enhancement applies to:

• SKU Scan and SKU Quantity receiving modes
• Pallet Handling Mode – **Palletize Upfront**

### New Hot Key to Show Receiving Details

A new Mobile hot key, **Ctrl-O: Show Details**, provides immediate access to shipment-level receiving metrics without leaving the current receiving transaction. The hot key is available from both the **Shipment Scan** and **SKU/Quantity Scan** screens and displays:

• SKUs Received for the Shipment
• LPNs Received for the Shipment
• Pallets Received for the Shipment

The displayed values are updated as receiving progresses and reflect inventory already received for the shipment. Default values of zero are displayed until receiving activity has occurred.

This enhancement supports:

• Cartonized and non-cartonized receiving
• PO-based receiving
• Detailed receiving
• SKU Scan and SKU Quantity receiving modes
• All pallet handling modes
• All receiving modes
• Quantity UOM receiving

Supported Mobile screens include:

• **Mobile Receive by Shipment** (rf.inbound.cwrfrecvlpnshpmt)
• **Mobile Receive by Load** (rf.inbound.cwrfrecvlpnload)
• **Mobile Receive Single SKU** (rf.inbound.cwrfrecvsinglesku)

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*