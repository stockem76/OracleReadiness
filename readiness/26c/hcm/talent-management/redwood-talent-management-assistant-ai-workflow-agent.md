[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Redwood: Talent Management Assistant AI Workflow Agent

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f49399.htm)

As managers, leverage the **Talent Management Assistant** AI workflow agent to get more information about your team members and obtain more insights about them. You can query this workflow agent to obtain these details about your team members:

• Talent ratings
• Prior ratings
• Feedback received
• Performance evaluation ratings
• Performance goals assigned and the progress on these goals
• Development goals assigned and the progress on these goals
• Check-in discussions
• Skills and qualifications
• Competencies

You can use this workflow agent through a guided journey. For example, you can invoke it from a guided journey on the manager’s Talent Review Meetings overview page.

## 🎯 Business Benefit

Leverage the Talent Management Assistant AI workflow agent to obtain comprehensive information about your team members and rate your team members better.

## ⚙️ Steps to Enable and Configure

Your environment must have certain necessary configurations. Ask your help desk to contact Oracle Support, who can verify what your environment has and address any gaps. For more information, see FAQ2521 on My Oracle Cloud Support.

Set these profile option values as indicated in the table.

Profile Option Name | Profile Option Code | Value
Enable Security Console External Application Integration | ORA_ASE_SAS_INTEGRATION_ENABLED | Yes
Enable VBCS Progressive Web Application User Interface | ORA_HCM_VBCS_PWA_ENABLED | Y
Redwood Guided Journey Setup Page Enabled | ORA_PER_GUIDED_JOURNEYS_SETUP_REDWOOD_ENABLED | Y
Agent Task Type Enabled for Guided Journeys | ORA_PER_AGENT_TASK_TYPE_GUIDED_JOURNEYS_ENABLED | Y

For more information about setting profile option values, see How do I enable a profile option?.

Enable permission groups for appropriate roles. For more information, see Access Requirements for AI Agent Studio.

To learn how to set up AI workflow agents, see Create AI Agents Using Preconfigured Agent Team Templates.

Create a guided journey task for the **Talent Management Assistant**AI workflow agent. For more information, see Configure Agent Task Type in Journeys. Note the guided journey code and add it to the guide journey page property of the page from which you want to invoke the **Talent Management Assistant**AI workflow agent. For example, on the manager’s Talent Review Meetings overview page you can add the guided journey code to the **Set Guided Journeys Code at the Page Level** page property. For more information, see Extend Application Page with Agent Guided Journey.

## 🔐 Access Requirements

The agents you can view depend on the roles and privileges assigned to you. To access this workflow agent, your role must be explicitly granted access to it by an AI Studio Administrator. For more information, see How can I give users access to AI agents and Access Requirements for AI Agent Studio.

## 📚 Key Resources

• Explore AI Agents for Oracle Fusion Cloud Applications
• How do I use AI Agent Studio?

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*