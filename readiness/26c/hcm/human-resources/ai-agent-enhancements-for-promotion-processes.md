[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Human Resources](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/human-resources.md)

# AI Agent Enhancements for Promotion Processes

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hure-26c/26C-hr-wn-f47397.htm)

Promote workers with the help of the AI-powered digital **Promotion Assistant**. The agent supports managers and HR teams in identifying and recommending eligible employees for promotion by automating the assessment process based on set parameters such as performance ratings, years of service, organization policies, collective agreements, or contracts. The AI agent guides users through the workflow, suggests suitable candidates, and brings consistency and transparency to the promotion process.

Built on Oracle’s AI Agent framework and powered by large language models (LLMs), the agent understands your natural language queries and responds with accurate, secure information based on your role and privileges. It also provides deep links to guide you directly to the relevant pages in Oracle Fusion HCM Cloud.

The **Promotion Assistant** is available in addition to the existing **Promotion Advisor**. While the Promotion Advisor continues to provide supervisor-agent-based guidance, the Promotion Assistant supports a workflow-agent experience for promotion actions and eligibility evaluation.

With the Promotion Assistant, you can additionally do these actions :

• Enable the agent to iterate through all direct reports of a manager based on the line manager relationship, evaluate each direct report for promotion eligibility, and generate a consolidated report.
• Include peer or colleague feedback in the promotion workflow to provide additional context for promotion recommendations.
• Auto-generate detailed assignment notes by merging eligibility rationale from the workflow agent with peer feedback and performance inputs.

**Sample Questions**

• Which of my direct reports are eligible for promotion this cycle?
• Evaluate all my direct reports for promotion eligibility and generate a consolidated report with rationale.
• Why is this employee eligible or not eligible for promotion based on tenure, performance rating, and promotion policy?
• Promote John Smith effective 1 July. 2026 to Senior Analyst, Grade IC3, update his salary to INR 18,00,000, and show the new pay and percentage increase before I submit.

Promotion Assistant

This feature improves the efficiency, consistency, and transparency of the promotion process. Managers can evaluate all direct reports in one request, review eligibility rationale, include peer feedback, and create more complete promotion recommendations before submission.

## ⚙️ Steps to Enable and Configure

• Your environment must have the appropriate services for Oracle Applications Platform deployed. For more information, see FAQ2521 on My Oracle Cloud Support
• Set the **Enable Security Console External Application Integration** (**ORA_ASE_SAS_INTEGRATION_ENABLED**) profile option to **Yes**, and enable permission groups for the appropriate roles. See Access Requirements for AI Agent Studio
• Resign from Employment is a preconfigured template. You need to create your own agent using the preconfigured template.

   To learn how to set up AI agents, see Create AI Agents Using Preconfigured Agent Team Templates.

You need to configure security to use this feature. See the *Access Requirements*section.

## 💡 Tips and Considerations

• The assistant supports updates for a single worker and one assignment. It doesn’t perform mass updates.
• If a worker has a pending transaction, the assistant displays a message and provides a link to review the pending transaction details.
• The assistant uses the existing Promotion approval process and doesn’t introduce a separate approval path.
• This is a predefined runnable agent.
• The option to customize this agent will be supported in future releases.

## 🔐 Access Requirements

The agents you can view depend on the roles and privileges assigned to you. To access this agent, your role must be explicitly granted access to it by an AI Studio Administrator. See How can I give users access to AI agents, and Access Requirements for AI Agent Studio.

## 📚 Key Resources

• Explore AI Agents for Oracle Fusion Cloud Applications
• How do I use AI Agent Studio?
• To learn how to set up AI agents, see Create AI Agents Using Preconfigured Agent Team Templates.

---
*Oracle Cloud Readiness · 26C · HCM · Human Resources*