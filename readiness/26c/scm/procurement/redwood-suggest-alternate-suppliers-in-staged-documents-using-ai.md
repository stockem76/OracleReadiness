[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Procurement](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/procurement.md)

# Redwood: Suggest Alternate Suppliers in Staged Documents Using AI

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/proc26c/26C-procurement-wn-f44485.htm)

Use AI to suggest alternate suppliers from historical transactions when processing requisition lines into a purchase order using the Redwood experience. These suggestions are derived from past transactions such as purchase orders, purchase agreements, negotiation awards, responses, and invitations.

When you create a staged document, you can initiate the **Suggest Alternate Supplier Using AI** action to view supplier suggestions. The AI model identifies relevant suppliers for each staged document line by matching attributes such as item, line description, or category. Suggested suppliers are consolidated and presented for inclusion in the staged document.

Suppliers are ranked based on the number of staged document lines they can fulfill. Lines without supplier suggestions are grouped under **Lines Not Covered** for targeted review.

Add Suggest Alternate Supplier Using AI

Buyers can review a confidence rating for each suggested supplier. This rating is based on a similarity score that measures how closely staged document line attributes, such as item, description, and category, match a supplier’s historical transactions. The overall supplier confidence rating is derived from the highest line-level rating across the staged document lines.

The similarity score ranges from 1 to 100 and is categorized as follows by default:

• High: 80 and above
• Medium: 60 to 79
• Low: 40 to 59

Supplier Suggestions Based on AI Model with Confidence Rating

Staged Document Lines Not Covered by Any of the Suggested Suppliers

You can evaluate a suggested supplier by clicking the supplier name. Any staged document lines that a suggested supplier can't fulfill are shown under **Lines Not Covered** for quick review.

Review Details of the Suggested Supplier

Staged Document Lines Not Covered by the Suggested Supplier

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Procurement*

• If you haven't enabled Redwood for Purchasing, see the Getting Started with Redwood in Purchasing topic on the SCM Resource Center in Customer Connect.
• Run the **Prepare Smart Supplier Suggestions** scheduled job to extract historical transactions and train the AI model to provide supplier suggestions. Consider scheduling this process to run periodically so the model can be refreshed as new approved purchasing document history becomes available.
• To adjust the default similarity thresholds, follow these steps:

1. In the Setup and Maintenance work area, search and select the **Manage Administrator Profile Values** task.
2. On the Manage Administrator Profile Values page, search for and select these profile option name or code: 
  • High AI Confidence Supplier Suggestions Threshold (ORA_PON_SUPPLIER_AI_HIGH_THRESHOLD)
• Medium AI Confidence Supplier Suggestions Threshold (ORA_PON_SUPPLIER_AI_MEDIUM_THRESHOLD)
• Low AI Confidence Supplier Suggestions Threshold (ORA_PON_SUPPLIER_AI_LOW_THRESHOLD)
3. Set the profile options values between 1 and 100.
4. Select **Save and Close**. Changes to the profile values take effect the next time users sign in.

## 💡 Tips and Considerations

• By default, the scheduled job extracts 24 months of historical transactions. You can modify this duration by updating the **ORA_PON_SUPPLIER_AI_NUM_OF_MONTH** profile option according to your business requirements. To update the duration, follow these steps: 
  1. In the Setup and Maintenance work area, go to the **Manage Administrator Profile Values** setup task.
2. Enter the **ORA_PON_SUPPLIER_AI_NUM_OF_MONTH** profile option code and search.
3. Update the profile option value and save.
• If a supplier has at least one high-confidence match, the overall rating is High.
• If no high-confidence matches exist but at least one medium-confidence match is found, the overall rating is Medium.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains this new privilege can run the ESS job:

• Configure Smart Supplier Recommendations (PON_CONFIGURE_RECOMMEND_SUPPLIERS_AI_PRIV)

## 📚 Key Resources

• For details on additional buyer capabilities available while processing requisition lines, see the Redwood: Use Additional Capabilities When Processing Requisition Lines as a Buyer, available in *Oracle Fusion Cloud Procurement What's New*, update 25C.
• For details on processing requisition lines using the Redwood user experience, refer to the Redwood: Search and Process Requisition Lines Using a Redwood Page, available in *Oracle Fusion Cloud Procurement What's New*, update 25B.

---
*Oracle Cloud Readiness · 26C · SCM · Procurement*