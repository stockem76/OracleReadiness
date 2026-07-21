[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# JPK Audit File for Poland Asset Register

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f40237.htm)

Generate the JPK_ST asset register section using the revised JPK_CIT audit file format for Poland. This report includes asset information from both accounting and tax asset books for the same asset records and follows the XML schema defined by the Polish tax authorities.

The JPK_ST report is submitted annually along with the JPK Accounting report under JPK_CIT. Use the existing scheduled process for JPK Accounting to generate the report by specifying values for these parameters:

• Corporate Asset Book
• Accounting Asset Book
• Tax Asset Book

All three parameters are required to generate the JPK_ST report. If asset book information isn’t provided, the process generates the JPK_PD Accounting file instead.

This requirement applies to transactions for the 2026 calendar year and onward, as mandated by the Polish Ministry of Finance.

• Ensures compliance with Poland's JPK_CIT statutory reporting requirements by enabling submission of asset register data in the required JPK_ST format.
• Supports accurate and complete reporting of accounting and tax asset data for fiscal year 2026 and beyond.

## ⚙️ Steps to Enable and Configure

No additional system configuration is required to run the report.

However, ensure that required lookup values and global descriptive flexfields (GDFs) are populated for asset transactions.

1. Add lookup values for CODE KST 2016 (provided by the tax authorities for each asset) using the ORA_JGPL_JPK_PL_ASSET lookup type. 
  • Use three-digit codes: 
    • 1st digit: Group
• 2nd digit: Subgroup
• 3rd digit: Type
2. Capture required GDF values for asset transactions during fiscal year 2026 so that they are available for extraction in January 2027.

• Asset Addition: Type of Purchase Document and KST code
• Depreciation Method: Depreciation Method for Poland
• Retirement: Reason for Retirement

Values for Purchase document type, KST code, and Depreciation method can be updated after the transaction. However, the retirement reason must be entered only during the retirement transaction.

All required GDFs and new parameters for the Asset books in the scheduled process are predefined.

## 💡 Tips and Considerations

• Maintain separate asset books for accounting and tax reporting as required by JPK ST.
• When the primary ledger is used for Poland tax reporting: 
  • Use the corporate asset book as the accounting asset book
• Use a separate tax asset book for tax reporting
• When using a global primary ledger and a Poland-specific secondary ledger with a different currency: 
  • Maintain two asset books for Poland: 
    • One for accounting purposes
• One for tax purposes

**Asset Updates:**

• You must enter GDF values for the purchase document type and KST classification for all active assets by January 1, 2026.
• You must maintain depreciation method GDF values for all asset categories across accounting and tax asset books.

**Retirements:**

• Record the retirement reason during each retirement transaction starting January 1, 2026.

   These values are used during JPK_ST report generation in 2027 to populate mandatory reporting fields.

## 🔐 Access Requirements

Same as the ones used for the existing JPK release.

## 📚 Key Resources

Refer to the JPK Extracts Topical Essay for detailed information on reporting requirements and GDF usage.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*