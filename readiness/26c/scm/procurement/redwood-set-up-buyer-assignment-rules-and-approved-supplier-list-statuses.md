[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Procurement](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/procurement.md)

# Redwood: Set Up Buyer Assignment Rules and Approved Supplier List Statuses

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/proc26c/26C-procurement-wn-f46550.htm)

Use Redwood pages to manage buyer assignment rules and approved supplier list statuses in Oracle Fusion Cloud Procurement.

On the Buyer Assignment Rules page, as a procurement administrator, you can create, update, view, delete, and test buyer assignment rules that automatically route requisition lines to the appropriate buyer based on rule criteria such as requisitioning business unit, procurement business unit, commodity, deliver-to organization, project, cost center, supplier, noncatalog request, and line amount. You can search for rules, review matching rule details, create rule sets, duplicate existing rules, and manage rules in a spreadsheet.

Buyer Assignment Rules

On the Approved Supplier List Statuses page, you can create, update, view, and delete statuses that describe the condition of approved suppliers. You can define statuses, assign a default status, and set end dates to control when a status becomes inactive.

Approved Supplier List Statuses

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Procurement*  No Longer Optional From: *Update 27A*

**Note:** The feature is enabled by default.

To manage the Purchasing setup pages, follow these steps:

1. In the Setup and Maintenance work area, search for and select one of these tasks: 
  • **Manage Buyer Assignment Rules**
• **Manage Approved Supplier List Statuses**
2. On the setup page, make the required changes.
3. Click **Save**or **Save and Close**.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access these features:

• Manage Buyer Assignment Rules (PO_MANAGE_BUYER_ASSIGNMENT_RULES_PRIV)
• Manage Approved Supplier List Status (PO_MANAGE_APPROVED_SUPPLIER_LIST_STATUS_PRIV)

These privileges were available prior to this update.

---
*Oracle Cloud Readiness · 26C · SCM · Procurement*