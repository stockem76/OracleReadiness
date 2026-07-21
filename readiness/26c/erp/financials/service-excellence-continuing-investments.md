[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Service Excellence Continuing Investments

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49371.htm)

Our ongoing investment in service excellence has a focus on overall usability, resiliency, performance, and security. This work is based on monitoring performance trends, reviewing common use patterns, analyzing service requests, and participating in many discussions with customers.

**Usability:**

**Credit to Cash - Credit to Cash Reporting for Prepayments:**

• You can now use a new Subledger Accounting (SLA) source, **Prepayment Line Type Code**, to more easily differentiate prepayment-related transaction lines during the accounting process. This enhancement improves flexibility when defining accounting rules for prepayments and their related activities.

The **Prepayment Line Type Code** source is available for both **Invoice** and **Credit Memo** event classes. You can use this source when configuring **journal line rules** and **accounting segment rules**, enabling more precise accounting for prepayment transactions.

The source supports the following values:

• Prepayment invoice line
• Prepayment application line
• Tax line for prepayment invoice line
• Tax line for prepayment application line
• Credit memo line for prepayment invoice line
• Credit memo line for prepayment application line
• Tax line for credit memo line on prepayment invoice line
• Tax line for credit memo line on prepayment application line

This enhancement helps you better classify and account for prepayment, application, credit memo, and associated tax lines, improving overall usability and control in accounting configurations.

**Record to Report - Accounting Processing:**

• Dynamic Accounting Period Scheduling for Multiperiod Accounting feature enables scheduled Create Multiperiod Accounting runs to automatically derive the Accounting Period at runtime. In addition to selecting a specific Open or Future period, users can choose Current Period, Earliest Open Period, or Latest Open Period. The process derives the applicable period based on the selected ledger, accounting calendar, user preference time zone, and period status. This removes the need to create separate schedules for each accounting period and supports chronological, period-based execution through dynamic period selection.

**Credit to Cash - Bill Management:**

• You can now download multiple transactions at once. You can select multiple transactions in the Bill Management Dashboard and click on print, which will give you a zip file with individual PDFs for each transaction.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*