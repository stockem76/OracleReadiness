[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Procurement](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/procurement.md)

# Selected Purchasing Bug Fixes in This Update

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/proc26c/26C-procurement-wn-f47268.htm)

This update includes some bug fixes that can change the way Oracle Purchasing works. This isn't a full list of all the bug fixes in this update. This list includes the bug fixes that can cause a noticeable change in application behavior.

**Funds Liquidation Period Determination for Past-Dated and Future-Dated Transactions**

In update 26, the Liquidate Funds and Encumbrance Using Change Order Budget Date or Current Date profile option (ORA_PO_CO_BUDGET_DATE_FOR_LIQ) is enhanced.

When the profile option is set to Y, the application uses these rules for change orders with funds liquidation:

• Change orders where the PO isn't partially fulfilled 
  • If the budget date is on or after the current date, funds are liquidated on the budget date.
• If the budget date is before the current date, funds are liquidated on the user-provided change order date.
• Change orders where the PO is partially fulfilled and the budget date can't be edited 
  • If the budget date is on or after the current date, funds are liquidated on the budget date.
• If the budget date is before the current date, funds are liquidated on the current date.

This profile option applies only to change orders. It doesn't apply to:

• Final Close
• Cancel

For Final Close and Cancel transactions, funds liquidation follows the Budgetary Control rule date setup, and liquidation occurs on the date defined in the rule date configuration.

For future-dated transactions, you can:

• Use a change order to modify the budget date before performing Final Close or Cancel, or
• Use Carry Forward to reopen the PO with a new budget date.

Oracle reference: 39046687

**Global Descriptive Flexfields (DFFs) for Approved Supplier List Source Documents**

You can now enable global descriptive flexfields (DFFs) for source documents on the Redwood Approved Supplier Lists page. You can navigate to the Approved Supplier List Entry Documents descriptive flexfield to create and configure global segments to capture additional standardized information across supplier list source documents.

  You can use Oracle Visual Builder Studio business rules to control the visibility of DFF segments and tailor the user experience on the Redwood Approved Supplier Lists page.

  Context sensitive descriptive flexfields for source documents aren’t supported.

Oracle reference: 38664375

**Back Arrow Navigation in the Redwood Purchasing Pages**

You can now use the back arrow on Purchase Orders, Purchase Agreements, and Requisitions Redwood pages to navigate back to the previous page across flows. In earlier releases, although the back arrow was available on these pages, navigation to the previous page wasn't supported in certain scenarios. Additionally, when these pages are accessed directly via URL, the back arrow redirects buyers to the Purchasing Landing Page.

Oracle reference: 38971350

**Review Charge Account Segment Details in Edit and Read-Only Modes**

Before this update, reviewing charge account combination details in the Redwood UI was difficult due to limited visibility and inconsistent tooltip behavior. With this update, you can easily review charge account details in both edit and read-only modes.

  In read-only mode, you can click the charge account link to review the charge account segment values in a scrollable list. This makes it easier to review all segment values, including those with longer descriptions.

  In edit mode, you can click the menu icon in the Charge Account field and select Combination Details to view the entered charge account segment details in a scrollable list. You can also search for and select a different charge account combination using the Search for combination menu option.

Oracle reference: 38504818

**Parameters Supported for Guided Journeys in Redwood Purchase Order Pages**

You can now add context-sensitive content to your Business Intelligence (BI) reports or URLs by using a page-level guided journey for these Redwood Purchase Order pages:

• Purchase Order – Edit
• Purchase Order – View
• Purchasing Document Changes

Use the parameters listed in this table to include context-sensitive content.

Redwood Page | Guided Journey Level | Supported Guided Journey Parameters
Purchase Order – Edit | Page | POHeaderId OrderNumber RequisitioningBUId RequisitioningBU DocumentStyleId DocumentStyle ProcurementBUId ProcurementBU SoldToLegalEntityId SoldToLegalEntity ChangeOrderNumber Language
Purchase Order – View | Page | POHeaderId OrderNumber RequisitioningBUId RequisitioningBU DocumentStyleId DocumentStyle ProcurementBUId ProcurementBU SoldToLegalEntityId SoldToLegalEntity Language
Purchasing Document Changes | Page | POHeaderId OrderNumber RequisitioningBUId RequisitioningBU DocumentStyleId DocumentStyle ProcurementBUId ProcurementBU SoldToLegalEntityId SoldToLegalEntity ChangeOrderNumber Language

Oracle reference: 39030659

**Redwood Page Navigation Update for Purchase Agreement Approval Notification**

Before update 26C, when you clicked the Purchase Agreement link in the Agreement approval notification, the application opened the ADF Classic View Purchase Agreement page instead of the Redwood View Purchase Agreement page. With update 26C, clicking the Purchase Agreement link in the Agreement approval notification now opens the Redwood View Purchase Agreement page.

Oracle reference: 39086304

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · SCM · Procurement*