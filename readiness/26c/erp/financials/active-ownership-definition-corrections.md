[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Active Ownership Definition Corrections

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f47297.htm)

Correct active ownership definitions and rebill affected joint venture transactions. This enhancement eliminates the need to end an active ownership definition and create a new one when ownership changes are required.

You can now modify ownership definitions even when they are in **Active** status. From the Ownership Definitions page, change the status to **Editing**, update effective dates or stakeholder ownership percentages, and save your changes. You can then return the definition to Active status to continue distributing joint venture transactions.

Editing status for Ownership Definitions

If the ownership definition has existing distributions, you must enter a Change Reason when making updates. You can also optionally provide additional details in the Change Reason Additional Information field. If no distributions exist, these fields remain unavailable.

Rebilling behavior for existing distributions:

• If you update effective dates, only transactions that fall outside the revised date range are redistributed and rebilled.
• If you update ownership percentages, all transactions associated with the ownership definition are rebilled.

Business Benefit:

Joint venture accountants can quickly correct active ownership definitions and accelerate the rebilling process resulting from the corrections.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• **Scheduled process behavior:** Downstream joint venture scheduled processes automatically ignore ownership definitions in Editing or Inactive status, preventing invalid processing.
• **Spreadsheet and work area support:** The Editing status is treated the same as the legacy Pending status in all joint venture work areas and VB Excel spreadsheets, so existing processes continue to function without modification. The same validations that applied to the former Pending status apply to the Editing status.
• **Security:**No new privileges are introduced, existing users with rights to manage joint venture definitions can perform these actions.

## 🔐 Access Requirements

No new access requirements.

## 📚 Key Resources

For more information, refer to:

• Implementing Joint Venture Management guide and
• Using Joint Venture Management guide.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*