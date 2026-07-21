[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Order Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/order-management.md)

# Redwood: View Program Checkbook for Supplier Rebate and Supplier Ship and Debit Programs

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/order26c/26C-order-mgmt-wn-f46540.htm)

Use a redesigned page that helps you view the financial balances of an individual supplier rebate or supplier ship and debit program more efficiently.

Realize these benefits:

• Improved responsive user interface for program managers
• Improved usability of program checkbook pages

Supplier Rebate Program

Supplier Rebate Accruals

Supplier Rebate Accrual Grouping Options

Supplier Rebate Accruals by Item

Supplier Rebate Transaction Accruals by Item

Supplier Rebate Accrual Related Payments

Supplier Rebate Payments

Supplier Rebate Transaction Accrual Column Personalization

Supplier Ship and Debit Program

Supplier Ship and Debit Accruals

Supplier Ship and Debit Accrual Grouping Options

Supplier Ship and Debit Accruals by Item

Supplier Ship and Debit Transaction Accruals by Item

Supplier Ship and Debit Accrual Related Payments

Supplier Ship and Debit Payments

Supplier Ship and Debit Transaction Accrual Column Personalization

Try it:

• Go to **Home**> **Order Management** > **Supplier Channel Management** > New Supplier Channel Management (from the Tasks panel tab) > Supplier Programs (New) > Programs. Select a program and select the Checkbook tab. Click **Earned**to drill down and view the transactional accruals.
• Using Quick Action: Go to **Home**> **Order Management** > **Show More** > Group **Supplier Channel Management** > Supplier Programs (New) > Programs. Select a program and select the Checkbook tab. Click **Earned**to drill down and view the transactional accruals.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Order Management*

1. If you haven't implemented Buy Side programs, then refer to the **Roadmap for Setting up Buy Side: Supplier Rebates**and**Roadmap for Setting up Buy Side: Supplier Ship and Debit** chapters in the **Implementing Channel Revenue Management**guide.
2. Run the scheduled process **ESS job to create index definition and perform initial ingest to OSCS**to create the index definition and perform initial ingest to Oracle Search with **fa-cjm-supplier-programs** as the parameter value.
3. Go to the Setup and Maintenance work area, then use the **Manage Administrator Profile Values** task to set the ORA_CJM_SUPPLIER_CHANNEL_REDWOOD_ENABLED profile option to Yes.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• **Manage Supplier Programs** (CJM_MANAGE_SUPPLIER_PROGRAMS_PRIV)
• **View Supplier Programs** (CJM_VIEW_SUPPLIER_PROGRAMS_PRIV)
• **Approve Supplier Programs** (CJM_APPROVE_SUPPLIER_PROGRAMS_PRIV)
• **Manage Channel Programs** using REST Service (CJM_MANAGE_CHANNEL_PROGRAMS_REST_SERVICE_PRIV)
• **Manage Channel Notes Data** (CJM_MANAGE_CHANNEL_NOTES_DATA)
• **View Only Activity** (ZMM_VIEW_ONLY_ACTIVITY_PRIV)

These privileges were available prior to this update.

## 📚 Key Resources

• For more information on Channel Revenue Management, refer to the **Oracle Cloud Readiness** content for **Order Management.**
• Oracle SCM Cloud: *Using Supplier Channel Management* guide available on the Oracle Help Center.
• Oracle SCM Cloud: *Implementing Oracle Channel Revenue Management* guide available on the Oracle Help Center.
• Oracle SCM Cloud: *REST API for Oracle SCM Cloud,* available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Order Management*