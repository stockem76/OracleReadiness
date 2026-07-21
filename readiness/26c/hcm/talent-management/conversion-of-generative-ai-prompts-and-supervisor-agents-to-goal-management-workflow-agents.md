[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Conversion of Generative AI Prompts and Supervisor Agents to Goal Management Workflow Agents

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f49463.htm)

Leverage these Goal Management workflow agents that are available on the **Agent Teams** tab of AI Agent Studio instead of the Generative AI prompts that were available in earlier releases:

• **Goal Creation  Assistant**: Creates a goal based on the goal name, the employee’s or manager’s department and business title. Suggests goals based on the manager’s comments in the previous performance evaluation. It replaces these  Generative AI prompts that are available in the AI Configurator tool: 
  • Performance goal creation
• Suggest goals from evaluation comments
• Team development goal creation
• Team performance goal creation
• Worker development goal creation
• **Team Goals Summary Generator**: Generates the summary of the manager’s teams goals. It replaces the **Team Goals Summary** Generative AI prompt that's available in the AI Configurator tool.

You can’t use the AI Configurator tool from now on to modify the generative AI prompts. You need to recreate the prompt customizations that were done for the generative AI prompts in the workflow agents.

Leverage these Goal Management workflow agents that are available on the Agent Teams tab of AI Agent Studio instead of the supervisor agents:

• **Employee Goals Assistant**: Assists employees in creating and managing their performance and development goals. It helps to answer employee queries about their performance and development goals.
• **Team Goals Assistant**: Assists managers in creating and managing their team’s performance and development goals. It helps to answer queries about the team’s performance and development goals.

These workflow agents dynamically interpret your intent based on your query and extract the required information. They have multiple nodes for performing specific functions.

Leverage these workflow agents to get these benefits:

• Create goals that are aligned with your organization’s objectives.
• Ensure a consistent goal setting process across your organization.
• Enable managers to easily follow-up on their team’s progress on the assigned goals.

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

Create a guided journey task for these workflow agents. For more information, see Configure Agent Task Type in Journeys. Note the guided journey code and add it to the guide journey page property of the page from which you want to invoke the workflow agent. For example, on an employee’s Goals Center page you can add the guided journey code to the **Set Guided Journeys Code at the Page Level** page property. For more information, see Extend Application Page with Agent Guided Journey.

## 💡 Tips and Considerations

These considerations apply when you use the Goal Management workflow agents:

• You can use the supervisor agents that were created in the earlier releases but note that these agents won’t be enhanced with the new functionalities that are available in the workflow agents. These supervisor agents now have the ‘_Deprecated’ suffix.
• You need to recreate the prompt customizations that were done for the Goal Management supervisor agents and generative AI prompts in the workflow agents.

## 🔐 Access Requirements

The agents you can view depend on the roles and privileges assigned to you. To access this agent, your role must be explicitly granted access to it by an AI Studio Administrator. For more information, see How can I give users access to AI agents and Access Requirements for AI Agent Studio.

## 📚 Key Resources

• Explore AI Agents for Oracle Fusion Cloud Applications
• How do I use AI Agent Studio?
• Deprecation of AI Configurator and Transition to AI Agent Studio

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*