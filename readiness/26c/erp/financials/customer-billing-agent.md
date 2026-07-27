[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Customer Billing Agent

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f50502.htm)

Use the Customer Billing Agent to retrieve customer billing information, including invoice details, payment status, and billing history, using natural language queries. The agent delivers real-time insights into customer open receivables, due dates, payments, and outstanding balances, reducing manual effort and improving response times. The agent streamlines inquiry handling and improves overall customer experience.

The Billing Inquiry, which is part of the Customer Billing Agent, enables faster, more accurate billing investigation by allowing users to ask natural language questions and receive focused, data-grounded responses without navigating across multiple Receivables work areas.

The agent improves operational efficiency by bringing invoice, customer account, dispute, credit memo, tax, currency, approval, and accounting inquiries into a single conversational experience. This reduces context switching, shortens investigation time, and helps users move from question to resolution more quickly.

These are the business benefits:

• Faster resolution of billing inquiries through guided, agent-assisted investigation
• Improved consistency and quality of responses across billing support interactions
• Reduced manual effort for teams handling repetitive billing questions
• Better user experience through clear, contextual, and actionable billing information
• Increased operational efficiency by helping teams focus on complex exceptions instead of routine inquiries

## ⚙️ Steps to Enable and Configure

The Customer Billing Agent shall be available by default under the ERP Agents workspace. Complete the required security prerequisites as referred to in the section 'Access requirements.'

## 💡 Tips and Considerations

• Billing Inquiry context doesn't support Insights or predefined prompts.
• Ask specific questions when possible. Include an invoice number, customer, account number, purchase order, sales order, dispute case, business unit, currency, or date range to narrow the response.
• Expect the response shape to vary by result count. A single result may return a field list, while multiple records may return detail rows or a rollup view.
• Use the filter context and totals to understand what was included, excluded, sorted, or grouped in the response.
• When multiple matching customers, invoices, or references are found, select the intended record before continuing the inquiry.
• Use the agent for inquiry and summarization. Continue any actions or activities in the appropriate Receivables page or workflow.
• Returned fields depend on source data availability, intent coverage, and the user's data-security assignments.

## 🔐 Access Requirements

The Billing Inquiry Assistant that is available as part of Customer Billing Agent is secured through an assistant duty role inherited by two Oracle-provided SAS-enabled Receivables Job Roles. Administrators must also enable permission groups in the Security Console.

**Oracle-provided Predefined Job Roles**

Seeded Job Role | Role Code
Billing Manager Segregated Role | ORA_AR_BILLING_MANAGER_JOB
Billing Specialist Segregated Role | ORA_AR_BILLING_SPECIALIST_JOB

**Billing Inquiry Duty Role**

Role | Role Code
Billing Inquiry Assistant | ORA_AR_BILLING_INQUIRY_ASSISTANT_DUTY

**Scenario 1 — If You Have Implemented Custom Job Roles**

  Use these steps for users who are not assigned one of the Oracle-provided predefined Receivables job roles listed above. To enable access, create or update a custom role with the required billing inquiry duty role.

1. Navigate to the Security Console.
2. Search for the custom job role you want to use.
3. Click Edit Role.
4. Select Enable Permission Groups.
5. Save your changes.
6. Navigate to Role Hierarchy > Roles and Privileges.
7. Add the Billing Inquiry Assistant duty role.
8. Navigate to Role Hierarchy > Roles and Permission Groups.
9. Add the same billing inquiry duty role that you added in the previous step.
10. Save your changes.

**Scenario 2 — If You Have Used Oracle-Provided Predefined Job Roles**

  Use these steps for users assigned one of the Oracle-provided predefined Receivables job roles listed above. These users inherit the corresponding billing inquiry duty role through their predefined job role. Administrators must still enable permission groups.

1. Navigate  to the Security Console.
2. Search for the applicable seeded job role, or the custom role derived from it.
3. Click Edit Role.
4. Select Enable Permission Groups.
5. Save your changes.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*