[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# Redwood: Correct Serial Number on a Drop Ship ASN

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f46483.htm)

Accurate serial number tracking is essential for traceability, compliance, and services or warranty tracking for organizations that rely on drop ship processes to fulfill customer demand. However, errors can occur occasionally when you create  Advance Shipment Notices (ASNs). For example, a supplier enters incorrect serial numbers resulting downstream issues in tracking, warranty, and service processes. You may face manual workarounds, delays, and data inconsistencies in the absence of an efficient way to correct such mistakes.

Now, you can correct the incorrect serial numbers entered on drop ship ASNs and the change is then reflected in the corresponding downstream flows, such as the sales order, genealogy, and outbound ASN.

Inbound Shipments

Click the **Edit**icon for a serial-control or lot-and-serial-control item. Enter the new serial number and new supplier serial number on the panel drawer.

Correct Serial Number

You can also view the history of serial number corrections by clicking the **Information**icon.

Serial number details -> View Serial Number History

This capability ensures that accurate serial information is maintained throughout the transaction lifecycle, improving data integrity, reducing operational disruptions, and enabling smoother downstream processing for tracking and customer support.

## ⚙️ Steps to Enable and Configure

• Add this new privilege (mentioned in Access Requirements section) to a custom role and assign the role to the applicable users.

## 💡 Tips and Considerations

• Corrected drop ship ASN serial numbers are interfaced to Shipping for reprinting shipping documents, to Order Management for future return order processing, to Install Base for maintenance, warranty, and to Genealogy for reporting.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains this privilege can access this feature:

• Correct Drop Ship ASN Serial Numbers (RCV_CORRECT_DROP_SHIP_ASN_SERIAL_NUMBERS_PRIV)

This privilege is new in this update.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: Using Receiving guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Security Reference for Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*