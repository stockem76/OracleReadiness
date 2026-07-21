[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# Redwood: View and Capture Additional Lot Attributes

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f46474.htm)

In industries where lot-controlled goods are widely used, timely and accurate entry of lot-level information is critical for maintaining product quality, ensuring compliance, and supporting informed decision-making. If you're unable to capture key lot attributes, such as expiration date, material status, or maturity date at the time of the transaction, this slows down operations and increases the risk of errors, inconsistent data entry, and fragmented information. Now, you have the ability to view and update lot attributes directly within the context of day-to-day transactions.

These editable lot attributes have been added to the Inventory and Receiving transactional pages:

**Inventory**

Page | Navigation | Additional Lot Attributes
Pending Transactions | Inventory Transactions > Pending Transactions > Record Lots | Material Status Supplier Lot (when existing lot is used for miscellaneous receipt)
Miscellaneous Transactions | Item Quantities > Create Miscellaneous Transactions > Record Lots | Miscellaneous Receipt: Material Status Supplier Lot (when existing lot is used for receipt) Miscellaneous Issue: Transaction Reason
Interorganization Transfer | Item Quantities > More Actions > Create Interorganization Transfer > Record Lots | Transaction Reason
Project Transfer | Item Quantities > More Actions > Create Project Transfer > Record Lots | Transaction Reason
Consigned Inventory | Transfer to Owned > Record Lots Transfer to Consigned > Record Lots | Transaction Reason
Picks | Picks > Pick Details > Record Lots | Transaction Reason
Confirm Pick Slips | Open Pick Slips > Pick Slip > Record Lots | Reason

**Receiving**

Page | Navigation | Additional Lot Attributes
Expected Shipment Lines | Expected Shipment Lines > Record Lots | When adding new lots: Material Status When selecting existing lots: Supplier Lot Reason
Awaiting Inspection | Received Lines > Awaiting Inspection > Record Lots | Reason
Awaiting Put Away | Received Lines > Awaiting Put Away > Record Lots | When adding new lots: Material Status When selecting existing lots: Supplier Lot (when lot wasn't entered at receipt) Reason
Corrections | Received Lines > Corrections > Record Lots | When selecting existing lots: Supplier Lot Reason

The **Generate Lot**, **Generate Parent Lot**, and **Generate Multiple Lots** action buttons have been added to these transactional pages where applicable:

**Inventory**

Page | Navigation | Additional Action Buttons
Miscellaneous Transactions | Item Quantities > Create Miscellaneous Transactions > Record Lots | Generate Lot Generate Parent Lot Generate Multiple Lots
Miscellaneous Transactions | Item Quantities > Create Miscellaneous Transactions | Generate Lot
Lots | Lots and Serial Numbers > Lots > New Lot | Generate Lot Generate Parent Lot

**Receiving**

Page | Navigation | Additional Action Buttons
Receive Lines | Expected Shipment Lines > Receive > Record Lots | Generate Parent Lot Generate Multiple Lots
Awaiting Put Away | Received Lines > Awaiting Put Away > Record Lots
Corrections | Received Lines > Corrections > Record Lots

You can now generate multiple lots with or without serial numbers. System-generated serial numbers are created in ranges. After generating the lots, you can choose to manually enter or scan the serial numbers.

Generate Multiple Lots

Lots and serial numbers are displayed in a tabbed structure, with serial numbers accessible through links.

Record Lots

This feature allows you to make necessary updates in real time, without disrupting your workflow, resulting in improved efficiency, more consistent data capture, and stronger support for traceability and regulatory compliance.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• The **Parent Lot** field and the **Generate Parent Lot** action button will be displayed only for child lot-controlled items.

## 🔐 Access Requirements

No additional access is required. Users with existing access to the Redwood Inventory and Receiving transactional pages can access this feature.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: Using Inventory Management guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Security Reference for Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*