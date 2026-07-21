[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# AutoApproved Multitier Intercompany Transaction

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49224.htm)

Automatically create intercompany transactions, intercompany invoices, and accounting entries by enabling autoapproval of intercompany transactions. This feature streamlines intercompany processing while maintaining the flexibility to apply manual controls when required.

A new Approval Flow column is available on the Intercompany Document Preparation page. Transactions default to a manual approval flow, allowing you to review and approve transactions using the existing process. You can now update the approval flow to autoapproval. When set to autoapproval, the application bypasses the approval step and automatically creates and completes transfer authorizations, processes transactions in Multitier Intercompany Operations without requiring manual approval, and generates intercompany journal entries or intercompany Receivables and Payables invoices.

This feature applies to:

• Intercompany transactions originating from Payables cross charge invoices, where invoice data is transferred to Document Preparation for intercompany processing.
• Transfer authorizations created directly in Multitier Intercompany Operations.

Intercompany Payables invoice creation remains manual by default to allow review and adjustment of intercompany Receivables invoices. You can optionally enable the automatic creation of intercompany Payables invoices.

These are the business benefits:

• Reduces manual effort by automating intercompany transaction processing.
• Accelerates transaction processing by eliminating manual approval steps.
• Processes high volumes of intercompany transactions without increasing manual effort.
• Improves data accuracy and consistency by minimizing manual intervention.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 🔐 Access Requirements

No new access requirements.

## 📚 Key Resources

• Multitier Intercompany Operations section in the Using General Ledger guide – To understand the flow of creating agreement, intercompany transfer authorization, intercompany transaction using the Multitier Intercompany Operations.
• Multitier Intercompany Operations topical essay - To learn more about the rationale for different types of intercompany transactions and for additional guidance on organizational structures.
• Automated Intercompany Cross Charge of Payables Invoice section in the Using General Ledger guide – To understand the processing of Payables cross charge invoices.
• How Payables Standard Invoice Import Data Is Processed section in the Using Payables Invoice to Pay guide – To understand the steps involved in creating invoices.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*