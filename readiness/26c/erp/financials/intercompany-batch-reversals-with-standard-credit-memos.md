[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Intercompany Batch Reversals with Standard Credit Memos

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f46535.htm)

Create Intercompany batch reversals that generate and automatically apply standard credit memos against the original receivable intercompany invoices. A new option is available to create and apply standard credit memos instead of on-account credit memo applications, to streamline the reversal process by eliminating the need for manual application of credit memos. This feature helps customers meet varying global regulatory requirements and is available for both batch-based and multitier intercompany transactions.

On-account credit memo (negative receivable transaction types) previously required manual application to the original invoice during intercompany batch reversals. Standard credit memos instead reference and apply directly to the invoice, removing the manual step. For both batch-based and multitier transactions, a new option is provided to generate standard credit memos instead of on-account credit memos.

Enable the new option on the Manage Intercompany Receivables Assignment to generate standard credit memos as the negative receivable transaction type. If not enabled, on-account credit memos are generated for intercompany batch reversals. While creating intercompany reversals, you have the option to override the default setting for generating standard or on-account credit memos at the individual intercompany reversal level. This feature applies when the intercompany transaction type has invoicing enabled. It is supported for batch-based transactions, multitier reversals, and cross-charge reversals generated from document preparation.

Business benefits include:

• Eliminate manual application of credit memos, reducing processing time and operational effort.
• Improve accuracy by automatically applying credit memos to the correct invoices, minimizing data entry errors.
• Streamline intercompany reversal processing across batch-based and multitier transactions.
• Support consistent and auditable intercompany processing to help meet global regulatory requirements.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Financials*  No Longer Optional From: *Update 26C*

• Use the Opt In UI to enable this feature. For instructions, see the Optional Uptake of New Features section of this document.

## 🔐 Access Requirements

No new access requirements.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*