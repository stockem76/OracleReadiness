[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Invoice Import with Supplier Bank Account Details Using Collaboration Messaging Framework

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49280.htm)

Import B2B XML invoices in Fusion Payables with supplier Remit-to Bank Account Number and Supplier IBAN using the Collaboration Messaging. The Collaboration Messaging inbound payload containing the supplier external bank account information, are interfaced to Fusion Payables.

B2B invoices that are exchanged between Sellers and Buyers electronically are interfaced to Fusion Payables using the Collaboration Messaging-Payables webservice. For suppliers with multiple bank accounts, Oracle customers need to be able to import Supplier invoices with the specific bank account. When the optional supplier external bank account number and IBAN are supplied in the inbound XML and pass validation, the invoice installment is automatically populated with those bank details, enabling direct electronic payments. If the values are omitted, the system looks for a primary bank account associated with the supplier.The AP web service now exposes the **ExternalBankAccountNumber** and **ExternalBankAccountIbanNumber** fields for transmission through Collaboration Messaging to the AP invoice interface. The corresponding columns, **EXTERNAL_BANK_ACCOUNT_NUMBER** and **EXT_BANK_ACCOUNT_IBAN_NUMBER,**already exist in the **AP_INVOICES_INTERFACE** table.

For French localization, Oracle customers rely on Collaboration Messaging to process inbound AP invoice messages that carry supplier external bank account details. Exposing **ExternalBankAccountNumber** and **ExternalBankAccountIbanNumber** in the AP web service delivers clear, measurable value: it enables customers to consistently select and transmit the correct bank account for suppliers with multiple accounts, strengthens compliance with French localization requirements, and reduces payment errors and rework by ensuring installments are populated with validated remit-to bank details. In scenarios where the invoice is marked **"Remit to Supplier"** without explicit bank details, the import will fall back to the primary bank account of the third party supplier linked to the invoice.

## 🎯 Business Benefit

Enables seamless import of B2B XML invoices with supplier bank account details (Remit-to Bank Account Number and IBAN) via the Collaboration Messaging, ensuring accurate and efficient supplier payments in Fusion Payables.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• The supplier external bank account number and IBAN fields are optional in the inbound XML; providing them results in direct population of the invoice installment’s bank details.
• If these fields are omitted, the system falls back to the primary bank account, preferring a site level account when both site and supplier primary accounts exist.
• Supplying values that fail format or validation checks will cause the import to be rejected, preventing erroneous payment information from being stored.
• For invoices marked “Remit to Supplier” without explicit bank details, the system uses the primary bank account of the third-party supplier associated with the invoice.
• The behavior applies to both matched and unmatched invoices processed through the Payables invoice import process.

## 📚 Key Resources

Based on Idea 708849 from the Idea Lab on Oracle Cloud Customer Connect.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*