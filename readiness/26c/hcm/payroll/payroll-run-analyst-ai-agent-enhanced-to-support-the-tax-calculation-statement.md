[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Payroll Run Analyst AI Agent Enhanced to Support the Tax Calculation Statement

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f49836.htm)

The **Payroll Run Analyst** agent was enhanced to support the Tax Calculation Statement functionality. It allows payroll administrators to ask natural-language questions about an employee's payroll tax deductions for a selected payroll run and get clear, context-aware answers. The AI agent now supports conversational access to tax-calculation data in the Person Results UI for Canada. Payroll administrators can ask what taxes were calculated, how a specific tax was calculated, or questions about the various components used in the tax calculation.

The agent supports both summary and detailed responses while keeping reported values consistent with the underlying payroll calculation data.

The agent provides both:

• **Real-time tax explanations**: Explains attributes used in tax calculations, formulas, and calculation steps in plain language
• **Contextual guidance**: Answers questions about tax terminology, rates, thresholds, and applied tax rules within the page context

The agent can respond in English or French based on the language of the question.

This feature helps payroll administrators resolve tax-related questions faster by providing plain-language, context-aware explanations from tax-calculation data, which reduces manual navigation and interpretation effort.

## ⚙️ Steps to Enable and Configure

If not done already, you must configure the Agent Guided Journey and extend the Person Results page with the Agent Guided Journey. For details, see these topics in the guide, **How do I set up AI Agents for Redwood pages?**

• Configure Agent Guided Journey
• Extend Application Page with Agent Guided Journey

**Note**: The name of the agent is the **Payroll Run Analyst**.

## 💡 Tips and Considerations

The **Payroll Run Analyst** agent was enhanced to support the Tax Calculation Statement functionality. It is owned and maintained by Global Payroll. A new business object function was added to the Global Payroll agent. When referring to the agent, we are referring to the **Payroll Run Analyst**.

When creating a prompt to retrieve tax deduction details, include the keywords **"Tax Calculation Statement"** to help the system locate the correct source information. For example: *"Retrieve the Tax Calculation Statement and give me the tax details and calculation results for tax type CPP."* Prompts that do not include **"Tax Calculation Statement"** may not return the expected tax deduction details or calculation results.

## 📚 Key Resources

Refer to these documents located on the Canada Information Center (KA144) for additional information.

• **Administering Payroll for Canada**
• CA – Payroll tab > Product Documentation > Payroll Guides > Administering Payroll for Canada

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*