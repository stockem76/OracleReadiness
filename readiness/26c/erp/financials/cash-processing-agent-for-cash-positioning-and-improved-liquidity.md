[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Cash Processing Agent for Cash Positioning and Improved Liquidity

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f50616.htm)

**Cash Processing Agent**

  The Cash Processing Agent for Cash Positioning and Improved Liquidity helps cash managers review daily liquidity through an insights-driven conversational experience. It provides near real-time visibility into cash position, bank balances, intraday balance movements, and accounts with cash shortfalls. Users can review the insight, ask natural language questions, drill into account and balance details, and take follow-up actions.

  The following sections describe how the agent delivers these business outcomes.

**Overview**

  •    Provides a centralized starting point where users can review cash position information, begin with an insight or natural language question, and move into the appropriate cash positioning flow.

  •    The Cash Positioning context covers overall cash position review, currency-level cash position inquiry by legal entity or bank account, and intraday shortfall investigation.

  •    Enables users to interact through Ask Oracle by selecting predefined prompt suggestions or by entering natural language questions. Users can choose from predefined prompts for frequent cash position queries and review the intraday shortfall insight.

  •    Provides summarized cash position results with account-level details and supporting balance information.

  •    Helps users move from liquidity risk awareness to review and follow-up without manually switching among multiple Cash Management pages.

Overview

Cash Position Overview

Predefined Prompts

**Cash Position**

  The Cash Processing Agent for Cash Positioning and Improved Liquidity supports daily liquidity management by helping users review current and near real-time cash positions across their authorized bank accounts and legal entities. Users can ask natural language questions such as:

• Show the overall cash position.
• Show the cash position in the legal entity currency
• Show the cash position in the bank account currency

The agent responds with summarized results, account-level details, supporting cash movement information, and recommended next steps.

Cash Position Results

**Insights**

• Users can review the intraday shortfall insight from the Cash Positioning experience and open the insight to continue the investigation through the conversational experience.
• The intraday shortfall insight identifies bank accounts where available cash is below the required target balance based on intraday actuals.
• Users can review affected accounts, currencies, balance variance, and support cash position details before taking any follow-up action.
• Follow-up actions may include reviewing the transactions causing the shortfall or reviewing surplus accounts to facilitate fund movements.

Insights

Business benefits include:

• Detects intraday balance shortfalls earlier so cash managers and treasurers can review affected accounts before the issue becomes operationally significant.
• Improves liquidity visibility by providing a consolidated view of cash position and currency wise view of cash position by legal entities, bank accounts.
• Reduces manual effort and context switching by bringing conversational inquiry, intraday shortfall insight, and account-level cash position details into a unified experience.
• Supports controlled decision-making by enforcing existing Cash Management security, data access, validations, approval rules, and audit requirements.

## ⚙️ Steps to Enable and Configure

• The Cash Processing Agent for Cash Positioning and Improved Liquidity is enabled by default.
• Configure the required security access described in the Access Requirements section so users can access the agent from the navigation menu entry.
• Define target or minimum balances for bank accounts where intraday shortfall monitoring is required.
• Ensure that intraday statement data is available for accounts where users expect current-day liquidity visibility.

## 💡 Tips and Considerations

• Existing Cash Management classic ADF pages remain available for detailed bank statement review, bank account setup, and actions that are outside the conversational experience.
• The current scope focuses on current-day and near-term liquidity review and inquiry around the transactions contributing to the variances.
• The intraday shortfall insight requires intraday bank statement and target balances defined at the bank account level.
• Users should refresh or rerun inquiries when intraday statements are received, or transaction data changes before taking follow-up action.

## 🔐 Access Requirements

The Cash Processing Agent for Cash Positioning and Improved Liquidity is secured through assistant duty roles inherited by the Cash Position Inquiry Assistant Duty role.

Oracle Provided Predefined Job Role

Predefined Job Role | Role Code | Description
Cash Manager | ORA_CE_CASH_MANAGER | Protects and develops the liquid assets of a company maximizing their use and return to the organization, including managing company funds, overseeing the allocation of cash balances, reviewing forecasted balances, and examining any shortages or overages.

Assistant Duty Roles

Assistant Duty Role | Role Code | Description
Cash Position Inquiry Assistant Duty | ORA_CE_CASH_POSITION_INQUIRY_ASSISTANT_DUTY | Cash position inquiry, intraday shortfall insight review, and analysis of affected balances and underlying transactions.

**Scenario 1 - If You Have Implemented Custom Job Roles**

Use these steps for users who aren't assigned one of the Oracle-provided predefined Cash Management job roles listed above. To provide access, create or update a custom role with the required assistant duty role.

1. Navigate the Security Console.
2. Search for the custom job role you want to use.
3. Select Edit Role.
4. Select Enable Permission Groups.
5. Save your changes.
6. Go to Role Hierarchy > Roles and Privileges.
7. Add Cash Position Inquiry Assistant Duty for cash position inquiry and intraday shortfall insight access.
8. Go to Role Hierarchy > Roles and Permission Groups and add the same assistant duty role if permission group enablement is required.

**Scenario 2 - If You Have Used Oracle-Provided Predefined Job Roles**

Users assigned predefined Cash Manager job role inherit the duty roles. Administrators must still confirm that the assistant runtime access, applicable assistant duty roles, permission groups, and data access are available for users who will use the agent.

If users need the intraday shortfall insight, explicitly verify that Cash Position Inquiry Assistant Duty is available through the assigned role hierarchy or through a custom role assigned to the users.

## 📚 Key Resources

• Oracle Help Center: Using Cash Management
• Oracle Help Center: Implementing Cash Management
• Oracle Help Center: AI Agent Studio: Setup and Access Guide
• Oracle Help Center: Security Reference for Financials: Cash Management roles, duties, and privileges
• Oracle Help Center: REST API documentation for Cash Management

---
*Oracle Cloud Readiness · 26C · ERP · Financials*