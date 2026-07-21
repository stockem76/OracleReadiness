[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Order Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/order-management.md)

# Redwood: Manage Supplier Claims

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/order26c/26C-order-mgmt-wn-f46543.htm)

Use a redesigned page that helps you manage your supplier claims more efficiently.

Realize these benefits:

• Improved smart search
• Improved responsive user interface for program managers
• Improved usability of claim pages

Supplier Claims

Claim Filters Part 1

Claim Filters Part 2

Claim Filters Part 3

Column Personalization

Saved Searches

Assign Claims

Generate Claim Extract

General Tab

Settlement Tab

Accruals Tab

Accrual Reversal

Confirmation Tab

Try it:

• Go to **Home**> **Order Management** > **Supplier Channel Management** > New Supplier Channel Management (from the Tasks panel tab)
• Using Quick Action: Go to **Home**> **Order Management** > **Show More** > Group **Supplier Channel Management** > Supplier Claims (New)

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Order Management*

1. If you haven't implemented Buy Side programs, then refer to the **Roadmap for Setting up Buy Side: Supplier Rebates**and**Roadmap for Setting up Buy Side: Supplier Ship and Debit** chapters in the **Implementing Channel Revenue Management**guide.
2. Run the scheduled process **ESS job to create index definition and perform initial ingest to OSCS**to create the index definition and perform initial ingest to Oracle Search with**fa-cjm-supplier-claims** as the parameter value.
3. Go to the Setup and Maintenance work area, then use the **Manage Administrator Profile Values** task to set the ORA_CJM_SUPPLIER_CHANNEL_REDWOOD_ENABLED profile option to Yes.

## 💡 Tips and Considerations

• In the current release, you can only view Supplier Ship and Debit and Supplier Rebate claims from the Manage Supplier Claims page. Support for Supplier Annual Program claims is planned for a future release.
• In the Redwood UI 
  • Only for Supplier Ship and Debit claims, you can view transaction-level accruals and related item details in the Accruals tab for individual accrual entries.
• Accrual removal and accrual reversal are supported only for Ship and Debit claims.
• Accrual associations are available only at the Program level. Viewing accrual associations by both Program and Item isn't supported.
• In the Classic UI, associations are displayed at the Program level and can be expanded to both the Program and Item levels for Supplier Ship and Debit, Supplier Rebate, and Supplier Annual Program claims. When expanded to the item level, each row is assigned a unique line number. With the introduction of the Redwood UI, these line numbers are no longer displayed in the Classic UI.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• **Manage Supplier Claims** (CJM_MANAGE_SUPPLIER_CLAIMS_PRIV)
• **View Supplier Claims** (CJM_VIEW_SUPPLIER_CLAIMS_PRIV)
• **Approve Supplier Claims** (CJM_APPROVE_SUPPLIER_CLAIMS_PRIV)
• **Extract Supplier Claims**(CJM_EXTRACT_SUPPLIER_CLAIMS_PRIV)
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