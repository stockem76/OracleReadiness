[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Budget Entry Creation from Revenue for Control Budget

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f47293.htm)

Assign a control budget when creating a budget from revenue using the Create Budget Entry from Revenue process. The assignment of a control budget aligns the expense budget scenario to a control budget when importing the budget into both Budgetary Control and General Ledger. This simplifies management of multiple budget scenarios by allowing assignment of revenue-derived budget amounts to an expense budget scenario based on the control budget's revenue funding rules.

Business benefits include:

• Adding the **Control Budget** parameter to the **Create Budget Entry from Revenue** process ensures that budget entries are created and updated only for the intended control budget and its corresponding budget scenario.
• This ensures each control budget is updated against the  specific scenario when more than one control budget exists. Organizations can maintain proper alignment between **Control Budgets**, **Budget Scenarios**, and the **General Ledger**, reducing reporting inaccuracies, reconciliation issues, and downstream budget control errors.
• This enhancement gives users better control over budget processing in multi-control-budget environments.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

A new parameter **Control Budget** has been added to the **Create Budget Entry from Revenue** process.  This parameter is not required. Review any scheduled processes or scripts that automatically run this program.

## 🔐 Access Requirements

No new access requirements.

## 📚 Key Resources

To learn more about the **Create Budget Entry from Revenue** process, see **Using Financials for the Public Sector: Automated Funding of Expense Budgets from Revenue**.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*