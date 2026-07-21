[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Redwood: Succession Planning Guide Workflow Agent

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f49443.htm)

As managers, leverage the **Succession Planning Guide** AI workflow agent available on the **Agent Teams** tab of AI Agent Studio to complete your succession planning tasks for your team. This agent dynamically based on your query interprets your intent and invokes the appropriate succession planning agent. Use this workflow agent to perform these tasks:

• Add an internal candidate to a succession plan.
• Add an external candidate to a succession plan.
• Make a candidate the interim successor of a succession plan.
• Remove the interim successor status of a candidate.
• Update the readiness of a succession plan candidate.
• Create an **Incumbent** type of succession plan.
• View all succession plans in which a person has been added as a candidate.
• Identify the effects of a person leaving the organization on current succession plans.
• Identify team members having critical roles.

BUSINESS BENEFITS

  Leverage the Succession Planning Guide AI workflow agent to enhance the succession planning in your organization by reducing bias and ensuring uniformity and transparency.  This workflow agent can analyze large candidate pools and help in the succession management of large enterprises.

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

## 💡 Tips and Considerations

If you change the default LLM, then the agent's responses might vary, and you might have to modify the prompt to get the desired results.

## 🔐 Access Requirements

The agents you can view depend on the roles and privileges assigned to you. To access this agent, your role must be explicitly granted access to it by an AI Studio Administrator. For more information, see How can I give users access to AI agents and Access Requirements for AI Agent Studio.

## 📚 Key Resources

• Explore AI Agents for Oracle Fusion Cloud Applications
• How do I use AI Agent Studio?

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*