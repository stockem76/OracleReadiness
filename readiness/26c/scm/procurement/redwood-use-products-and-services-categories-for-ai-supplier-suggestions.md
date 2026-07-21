[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Procurement](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/procurement.md)

# Redwood: Use Products and Services Categories for AI Supplier Suggestions

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/proc26c/26C-procurement-wn-f46454.htm)

Invite AI-suggested suppliers to negotiations. The suggestions now include suppliers matched with products and services categories in their supplier profile. Update 25D introduced the ability to use AI Assist to generate supplier suggestions from past transactions such as purchase orders, purchase agreements, negotiation awards, responses, and invitations by matching the negotiation line item, line description, and category. In this update, supplier suggestions are expanded further by evaluating products and services categories defined in supplier profiles to identify additional suppliers relevant to the goods or services in the negotiation.

Supplier suggestions can now include suppliers whose profile categories match negotiation lines even with limited or no transaction matches. For example, when creating a negotiation for marketing services or IT equipment, the action **Add Suggested Suppliers** finds suppliers associated with related products and services categories in their profile. This will help you discover additional suppliers that you haven't transacted with before to include on the invitation list.

Add Supplier Suggestions

Supplier Suggestions Based on Past transactions and Supplier Profile Categories

Click on the supplier link to see details. You can quickly identify the suppliers with past transactions (suppliers with no transactions have supplier profile category matches). The confidence rating for a supplier reflects the highest-confidence match across the covered negotiation lines. The Purchasing Document count shows the number of past purchase orders and purchase agreements that matched with high confidence across the covered negotiation lines. Under Lines Covered, you can review the negotiation lines associated to the supplier. Lines that don’t have matching supplier suggestions are displayed under Lines Not Covered.

Suggested Supplier Details with Confidence Rating and Lines Covered

Drill down to lines covered to see key details and explanation about why this supplier was suggested. You can see the source, closest matching category, and confidence rating for the match along with key info on transactions and eligibility.

This enhancement helps category managers discover qualified suppliers more efficiently, especially for negotiations where direct item transaction history may be limited. By adding supplier profile products and services categories based matches to supplier suggestions, you can identify more relevant suppliers, reduce manual supplier research, and build stronger negotiation invitation lists faster.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Procurement*

To use this feature, you must opt in to both features:

• 25D feature**Redwood: Add Suppliers Suggested by Oracle AI**if you haven't already
• 26C feature**Redwood: Use Products and Services Categories for AI Supplier Suggestions**

For detailed instructions, refer to the Steps to Enable sections in the **What's New** for the update 25D .

Additionally, to use this feature, you must enable these profile options if you haven't already.

• Redwood Pages for Sourcing Enabled (ORA_PON_SOURCING_REDWOOD_ENABLED).
• Redwood Page to Create Negotiation Enabled (ORA_PON_CREATE_NEGOTIATION_REDWOOD_ENABLED)

For instructions on updating a profile option, refer to the Set Profile Option Values topic.

## 💡 Tips and Considerations

The quality of supplier suggestions generated from products and services category matches depends on how well products and services categories are maintained in supplier profiles. If products and services categories aren’t set up or aren’t maintained correctly for some suppliers, those suppliers may not be considered for supplier suggestions. We recommend reviewing and improving supplier products and services in the supplier management module as best practice to derive value from this feature.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Create Supplier Negotiation (PON_CREATE_SUPPLIER_NEGOTIATION_PRIV)
• Edit Supplier Negotiation (PON_EDIT_SUPPLIER_NEGOTIATION_PRIV)

These privileges were available prior to this update.

## 📚 Key Resources

• Refer to the update 25D What's New for the **Redwood: Add Suppliers Suggested by Oracle AI**feature.
• Refer to the update 26B What's New for the **Redwood: Confidence Rating for Suppliers Suggested by Oracle AI**feature.

---
*Oracle Cloud Readiness · 26C · SCM · Procurement*