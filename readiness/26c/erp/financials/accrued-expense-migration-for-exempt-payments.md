[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Accrued Expense Migration for Exempt Payments

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f47388.htm)

Import midlife leases with exempt payments by capturing accrued expense migration balances and recognizing exempt payments as expenses evenly over the remaining lease term. Periodic expenses are calculated by dividing the total exempt payment, net of accrued expense migration balance, by the number of remaining periods.

To create an expense lease with accrued expense migration balance for exempt payments:

1. Create an expense lease for property or equipment.
2. Update lease details to enable the Migrated Lease option.
3. Add an asset and an exempt payment to the lease. To add an exempt payment, the lease classification must be Exempt or the Right-of-Use and Lease Liability options on the payment must be unchecked.
4. Navigate to the Accounting tab in the Payment Details page.
5. In the Exempt Expense section, select the Amortize Over Term option and enter the Accrued Exempt Expense for the Primary or Secondary representation as applicable under Migration Balances. The Accrued Exempt Expense is the difference between the exempt expense accrual and payment amounts prior to the Amortization Start Date.
6. Validate the lease and generate schedules.
7. Use the Schedules tab to view the expense recognition schedule before lease activation.

The following screenshots describe the process of creating an exempt lease with accrued exempt expense migration balance:

Lease Details Page

Payment Details page

Payment Details Accounting tab

Schedules - Amortization Summary

Business benefits include:

• Ensure compliance with accounting standards by providing accurate and consistent expense recognition over the lease term.
• Reduce operational errors by standardizing the migration and expense recognition process for leases with exempt payments.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 🔐 Access Requirements

No new access requirements.

## 📚 Key Resources

Based on Idea 930639 from the Lease Accounting Idea Lab on Oracle Cloud Customer Connect.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*