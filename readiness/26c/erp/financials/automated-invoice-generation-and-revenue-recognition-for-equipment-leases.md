[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Automated Invoice Generation and Revenue Recognition for Equipment Leases

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f47389.htm)

Automatically generate periodic invoices and recognize revenue for equipment leases.

LEASE INVOICE PROCESSING

Lease administrators can invoice lessees for rent, service, maintenance, and other charges defined in the lease. Lease payments are transferred to Oracle Fusion Receivables to create invoices.

The Process Equipment Revenue Lease Payment process provides the ability to:

• Auto-approve and Transfer payments to the Receivables Interface. Transfer all draft payments or limit the transfer to a single lease, or to payments within a specific date range, or to payments for a particular customer and bill-to site, payment type, or payment purpose.
• Launch Receivables Invoice Import AutoInvoice as part of the lease process.
• Put payments on hold and subsequently release the hold.

The invoice number is available on the Schedules tab for a lease after the payment interfaces to Receivables and the Process Equipment Revenue Lease Payment Tie Back process is run.

The following screenshots describe processing payments for equipment revenue leases and reviewing payment schedules with drilldown to Receivables Invoices:

Side-Panel - Revenue Lease Payments

Process Payments for Equipment Revenue Leases

Process Payment Tiebacks for Equipment Revenue Leases

Schedules - Payment Schedules

LEASE REVENUE RECOGNITION

Recognize lease revenue each period according to lease accounting standards. When the Lease Administrator creates the lease, the revenue recognition schedule is automatically generated. For operating leases, the revenue is evenly spread over the revenue recognition term. The lease revenue recognition process creates the transaction to reduce the accrued asset balance and recognizes the revenue according to the schedule.

The following screenshots describe processing accruals for equipment revenue leases and reviewing accrued revenue schedules:

Side-Panel - Accounting

Process Accruals for Equipment Revenue Leases

Schedules - Accrued Revenue

Business benefits include:

• Ensure compliance with lease accounting standards for equipment revenue leases.
• Increase productivity and reduce errors through automated invoice generation and revenue recognition.
• Minimize manual effort in billing and collections via automated integration with Oracle Receivables.
• Enhance transparency by making Receivables invoices from Lease Accounting visible within lease record.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Financials*  No Longer Optional From: *Update 27A*

If you plan to adopt this feature, then you must log an SR with Oracle Support to get a code.

## 🔐 Access Requirements

No new access requirements.

## 📚 Key Resources

Based on Idea 639735 from the Lease Accounting Idea Lab on Oracle Cloud Customer Connect.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*