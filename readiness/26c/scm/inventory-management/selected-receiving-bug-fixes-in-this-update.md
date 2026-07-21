[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# Selected Receiving Bug Fixes in This Update

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f49930.htm)

This update includes some bug fixes that can change the way Oracle Receiving works. This isn't a full list of all the bug fixes in this update. This list includes the bug fixes that can cause a noticeable change in application behavior.

**Populate Additional Date Columns in Receiving Receipt Import FBDI**

For this update, additional date columns have been added after END in the RCV_TRANSACTIONS_INTERFACE csv file. The **Transaction Date** and **Expected Receipt Date** columns are now populated after END when the csv zip file is created and loaded to the interface.

Oracle reference: 38484904

**Add Invoice ID to the Confirm Receipts Notification BIP Report Data Model**

In order for system integrators to update reports and implement deep links to the View Invoice UI, now the Invoice ID has been added to the data model for the Confirm Receipts Notification under the Invoice Details section.

Oracle reference: 39223902

**Add Attachment When Overriding Distributions**

Prior to this update, users received receipt creation errors on the Redwood Orders to Receive page when overriding the distribution amount and adding an attachment to the distribution line. With this update, this issue has been resolved. Now when you select the **Override distribution quantities** option, you can upload an attachment and submit the transaction successfully. The attachment is associated with the first distribution line transaction.

Oracle reference: 38968422

**Hide Additional Information Region on Expected Shipment Lines Page**

For this update, you can hide the Additional Information region on the Expected Shipment Lines Redwood page. The business rule fields corresponding to the additional information columns are now present in Visual Builder Studio.

Oracle reference: 38937053

**Create Multiple Lot Numbers for Same ASN Line**

Prior to this update, when creating multiple lots for the same ASN line on the Redwood ASN page using the **Done** or **Next Option** buttons, the **Lot Number** field cleared the user input and only accepted input entry after a delay. With this update, users can now record multiple lots for same ASN line on the Redwood ASN page.

Oracle reference: 38449831

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*