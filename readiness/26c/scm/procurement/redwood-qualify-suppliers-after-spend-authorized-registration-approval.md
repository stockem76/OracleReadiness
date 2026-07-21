[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Procurement](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/procurement.md)

# Redwood: Qualify Suppliers After Spend Authorized Registration Approval

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/proc26c/26C-procurement-wn-f42794.htm)

When registering suppliers as spend authorized, you can gather questionnaire responses that are used to evaluate qualifications in Supplier Qualification Management. You can also automatically create qualifications after the registration request is approved, allowing qualification reviews to begin before spend authorization approval.

Spend authorized approval is a subsequent approval process after registration that you use to ensure the supplier is ready for procure to pay transactions. This feature allows approvers to review the qualifications that resulted from the registration process, ensuring the supplier is ready to proceed for spending.

Creating qualifications earlier in the process also improves supplier onboarding controls by separating registration based qualification review from the qualification reviews related to supplier promotion that happen later.

Prior to this update, a single qualification initiative was created after spend authorization approval. This initiative included qualification areas from these rule set events:

• Registration
• Registration Approval
• Supplier Promotion

With this update, qualifications and initiatives are created at two different events:

• After the registration request is approved, qualifications from registration and an initiative for registration approval are created. It creates qualifications for the qualification areas configured for the Registration event in the rule sets. This gives approvers visibility into qualification results before the supplier is authorized for spend.
• After the spend authorization request is approved, another initiative for supplier promotion is created. It creates qualifications for the qualification areas configured for the Supplier Promotion event in the rule sets.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Procurement*

## 💡 Tips and Considerations

There’s no change to the prospective supplier registration flow. This feature applies only to the spend authorized supplier registration flow.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Search Supplier Qualification Initiative (POQ_SEARCH_SUPPLIER_QUALIFICATION_INITIATIVE_PRIV)
• View Supplier Qualification Initiative (POQ_VIEW_SUPPLIER_QUALIFICATION_INITIATIVE_PRIV)
• Monitor Supplier Qualification Initiative (POQ_MONITOR_SUPPLIER_QUALIFICATION_INITIATIVE_PRIV)
• Search Supplier Qualification (POQ_SEARCH_SUPPLIER_QUALIFICATION_PRIV)
• Evaluate Supplier Qualification (POQ_EVALUATE_SUPPLIER_QUALIFICATION_PRIV)

Users who are assigned a configured job role that contains these privileges can search and update the rule sets:

• Search Supplier Registration Rule Set (POQ_SEARCH_SUPPLIER_REG_RULE_SET_PRIV)
• Edit Supplier Registration Rule Set (POQ_EDIT_SUPPLIER_REG_RULE_SET_PRIV)

These privileges were available prior to this update.

---
*Oracle Cloud Readiness · 26C · SCM · Procurement*