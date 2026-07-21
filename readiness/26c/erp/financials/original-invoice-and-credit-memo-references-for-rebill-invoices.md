[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Original Invoice and Credit Memo References for Rebill Invoices

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49248.htm)

Use the Rebill Source Transaction field in the Create or Edit Transaction page to associate a rebill invoice with its original invoice, improving traceability during rebill transactions.

When creating or editing a rebill invoice, enter the original invoice in the Rebill Source Transaction field. If creating the rebill invoice using the user interface, select the original invoice from the list of values. If creating the rebill invoice using AutoInvoice or REST services, populate the rebill source transaction details on the interface line or payload.

The application validates that the referenced invoice is eligible for rebilling. After the rebill invoice is completed, the Rebill Source Transaction field becomes read-only, and you can drill down to the source transaction to review details. From the source transaction, review related credit memo information in the Transaction Activities window.

These are the business benefits:

• This feature improves audit traceability and supports regulatory compliance by enabling you to explicitly associate rebill invoices with their source transactions.
• It reduces manual reconciliation effort, minimizes errors, and provides better visibility into transaction relationships across systems.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• The Rebill Source Transaction field only contains transactions of the Invoice transaction class.
• The field is available for all rebill invoices, including those invoices created without performing a credit application against the original invoice.
• The referenced original invoice must exist and be complete.
• The Rebill Source Transaction field becomes read-only after the rebill invoice is completed, and drill-down is available only after completion.
• The rebill source transaction reference isn’t supported using Receivables SOAP services.

## 🔐 Access Requirements

No new access requirements.

## 📚 Key Resources

Refer to the REST API for Oracle Financials Cloud documentation for details on Receivables transaction services.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*