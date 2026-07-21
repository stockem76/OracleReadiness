[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Liability Reclassification Calculation Options for Negative Short-Term Liability

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f47390.htm)

Configure alternate calculation methods for reclassifying lease liabilities using the Amortized Liability Balance approach. Choose between Simple Amortized Liability Balance and Adjusted Amortized Liability Balance methods to break out the lease liability into short-term and long-term for disclosure reporting.

Simple Amortized Liability Balance determines short-term liability by aggregating payments for the next 12 months minus the sum of interest expenses for the same period. The long-term liability is then calculated as the difference between the total discounted lease liability at the current month-end and the short-term liability.

Adjusted Amortized Liability Balance applies the same calculation methodology but reports the month-end short-term liability as zero if the calculated short-term liability value is negative and the total discounted lease liability at the current month-end remains positive. In such cases, the entire discounted lease liability balance at the current month-end is classified as long-term liability.

   

  Select the appropriate lease liability reclassification method based on your organization’s accounting policy.

Business benefits include:

• Automates the reclassification of lease liabilities, reducing manual effort and errors.
• Improves efficiency and saves time at period-end by streamlining liability calculations.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Financials*  No Longer Optional From: *Update 27A*

To enable this feature:

1. Navigate to the Manage Lease Accounting Configuration for the relevant business unit.
2. Locate the Liability Reclassification Method system option.
3. Select one of the available methods based on your organization’s accounting policy.

The following screenshot describes configuring the Liability Reclassification Method system option:

Configure System Options page

## 💡 Tips and Considerations

• The Liability Reclassification Method Amortized Liability Balance is now upgraded as the Adjusted Amortized Liability Balance.
• A one-time system options update may be done to change the Liability Reclassification Method from Short-Term Present Values to either Adjusted Amortized Liability Balance or Simple Amortized Liability Balance methods.
• A one-time system options update may be done to change the Liability Reclassification Method from Adjusted Amortized Liability Balance to Simple Amortized Liability Balance method.

## 🔐 Access Requirements

No new access requirements.

## 📚 Key Resources

Based on Idea 818983 from the Lease Accounting Idea Lab on Oracle Cloud Customer Connect.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*