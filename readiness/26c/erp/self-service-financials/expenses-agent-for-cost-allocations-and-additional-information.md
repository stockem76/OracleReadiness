[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Self Service Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/self-service-financials.md)

# Expenses Agent for Cost Allocations and Additional Information

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/ssfin26c/26C-ssfin-wn-f49363.htm)

Use the Expenses Agent to split expenses across cost centers, projects, and tasks, monitor monthly and annual spending limits, and support Flexible Key Flexfields (KFFs) by displaying selected accounting segments in the Redwood-themed Progressive Web App (PWA). These enhancements improve the accuracy of expense allocation and accounting.

• **Expense splitting:** Employees can split expenses across cost centers or assign them to projects and tasks.

Splitting an expense across accounts.

Note: Splitting expenses to project and task will be available in 26C Cohort B.

• **Flexible Key Flexfields**: Employees can charge expenses to the accounting segments configured for their business. 
  
Charge to configured accounting segments.
• **Monthly and Yearly Limits:** Monthly and yearly spending limits for Entertainment and Miscellaneous expenses are now supported.

Monthly limit validation

Business benefits include:

• Split Allocation enables accurate distribution of expenses across accounts or across projects and tasks, improving cost tracking and increasing productivity.
• Flexible KFF improves the expense entry experience by allowing only relevant accounting segments to be displayed in the PWA UI or captured through email, reducing complexity and improving completion accuracy.
• Monthly and yearly limits help enforce spending policies by controlling expenses within defined thresholds, improving compliance with organizational expense policies.

## ⚙️ Steps to Enable and Configure

To use these capabilities, first enable Expenses Agent as outlined in the Expenses Agent Detailed Adoption Guide.

**Flexible Key Flexfields:**

1. Assign the **Expense Override Segment** label to the accounting segments you want employees to use in the Redwood interface.

1. Sign in as an **Application Implementation Consultant**.
2. Navigate to **Setup and Maintenance**.
3. Open the **Manage Key Flexfields** task.
4. Search for the **General Ledger Key Flexfield** with code **GL#**.
5. Click **Manage Structures**, then edit the applicable structure.
6. Select the required segment and click **Edit**.
7. Assign the required segment labels. Select **Expense Override Segment** where applicable.
8. Click **Save and Close**.

2. From the **Manage Key Flexfields** page, deploy the General Ledger Key Flexfield.

3. Enable lookup **EXM_39687658**.

1. Navigate to **Setup and Maintenance**.
2. Search for and open **Manage Standard Lookups**.
3. Search for lookup type **ORA_ERP_CONTROLLED_CONFIG**.
4. In Lookup Codes table, select **Actions > New**.
5. Create and save a lookup code for **EXM_39687658**.

4. Wait at least one hour before continuing to the next step.

5. From the **Manage Key Flexfields** page, deploy the General Ledger Key Flexfield again.

6. Enable lookup **EXM_39339003**.

1. Navigate to **Setup and Maintenance**.
2. Search for and open **Manage Standard Lookups**.
3. Search for lookup type **ORA_ERP_CONTROLLED_CONFIG**.
4. In Lookup Codes table, select **Actions > New**.
5. Create and save a lookup code for **EXM_39339003**.

**Note:** If Segment Value Security by Business Function (SVSBF) is enabled, you can’t use the Flexible Key Flexfield feature.

• **Monthly/Yearly Limits:**
• Monthly and yearly limits are applicable to the Miscellaneous and Entertainment expense type. 
    • Use the steps outlined in the Entertainment Expense Policy document to set up an entertainment expense with a yearly policy limit.
• Use the steps outlined in the Miscellaneous Expense Policy document to set up a miscellaneous expense with both monthly and yearly policy limits.

## 🔐 Access Requirements

No new access requirements.

## 📚 Key Resources

• Expenses Agent general adoption guide.
• Expenses Agent detailed adoption guide.

---
*Oracle Cloud Readiness · 26C · ERP · Self Service Financials*