[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Conversion of Feedback Generative AI Assist Prompts to Workflow Agents

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f50139.htm)

Leverage these Feedback workflow agents in AI Agent Studio for AI Assist generated feedback. These agents replace the earlier Generative AI prompts used for creating feedback and the feedback summary.

• **Agent Teams**
• **Feedback Center Feedback Summary Generator** - Generates a combined summary of anytime and requested feedback to display on a workers Feedback Center
• **Anytime Feedback Generator** - Generates an enhanced anytime feedback comment for a worker
• **Requested Feedback Response Generator -**Generates a response to a question in a questionnaire requesting feedback for a worker

The transition to the new agents is required and will happen automatically as part of this release, so no opt-in or manual action is needed however, you can’t use the AI Configurator tool from now on to modify the generative AI prompts and will need to recreate the prompt customizations that were done for the generative AI prompts in the workflow agents.

Use these workflow agents to support feedback generating experiences such as:

• Generating a combined summary of anytime and requested feedback to display on a workers Feedback Center
• Generating an enhanced anytime feedback comment for a worker
• Generating a response to a question in a questionnaire requesting feedback for a worker

## ⚙️ Steps to Enable and Configure

Your environment must have certain necessary configurations. Ask your help desk to contact Oracle Support, who can verify what your environment has and address any gaps. For more information, see FAQ2521 on My Oracle Cloud Support.

Set these profile option values as indicated in the table.

Profile Option Name | Profile Option Code | Value
Enable Security Console External Application Integration | ORA_ASE_SAS_INTEGRATION_ENABLED | Yes
Enable VBCS Progressive Web Application User Interface | ORA_HCM_VBCS_PWA_ENABLED | Y

For more information about setting profile option values, see How do I enable a profile option?.

Enable permission groups for appropriate roles. For more information, see Access Requirements for AI Agent Studio.

To learn how to set up AI workflow agents, see Create AI Agents Using Preconfigured Agent Team Templates.

## 💡 Tips and Considerations

This consideration applies when you use the Feedback workflow agents:

• You need to recreate the prompt customizations that were done for the generative AI prompts in the workflow agents.

## 🔐 Access Requirements

The agents you can view depend on the roles and privileges assigned to you. To access an agent, your role must be explicitly granted access to it by an AI Studio Administrator. For more information, see How can I give users access to AI agents and Access Requirements for AI Agent Studio.

## 📚 Key Resources

• Explore AI Agents for Oracle Fusion Cloud Applications
• How do I use AI Agent Studio?
• Deprecation of AI Configurator and Transition to AI Agent Studio

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*