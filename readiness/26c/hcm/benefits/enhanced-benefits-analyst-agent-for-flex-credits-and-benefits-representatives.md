[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Benefits](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/benefits.md)

# Enhanced Benefits Analyst Agent for Flex Credits and Benefits Representatives

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/benf-26c/26C-benefits-wn-f49784.htm)

The Benefits Analyst Agent now includes additional tools to answer more Benefits-related questions for employees.

With this enhancement, the agent can:

• Answer questions about flex credit details using the flex credit summary tool. Flex credit details are retrieved as of the current date.
• Answer questions about benefits representatives using the Benefits Representatives’ Tool. This tool supports questions related to Benefits areas of responsibility.

The agent continues to answer questions only for the logged-in employee. Employees can't use the agent to ask for another employee's benefits information.

This enhancement gives employees more complete benefits-related answers in the existing Benefits Analyst Agent. Employees can get flex credit and benefits representative information without navigating away from the agent experience.

## ⚙️ Steps to Enable and Configure

This feature is available in the Redwood Benefits experience.

Enable these profile options. To learn how to enable a profile option, see How do I enable a profile option?.

• ORA_HCM_VBCS_PWA_ENABLED
• ORA_BEN_SELF_SERVICE_ENROLLMENT_REDWOOD_ENABLED

Your environment must have the appropriate services for Oracle Applications Platform deployed. For more information, see FAQ2521 on My Oracle Cloud Support.

Set the **Enable Security Console External Application Integration** (**ORA_ASE_SAS_INTEGRATION_ENABLED)** profile option to Yes, and enable permission groups for the appropriate roles. See Access Requirements for AI Agent Studio.

To learn how to set up AI agents, see Create AI Agents Using Preconfigured Agent Team Templates.

To learn how to enable AI Agents, see Enable AI Agent in Redwood Benefits Pages

## 💡 Tips and Considerations

• Flex credit details are retrieved as of the current date.
• The agent answers benefits representative questions using the benefits representatives tool.
• The agent answers questions only for the logged-in employee.
• The agent doesn't provide benefits information for other employees.
• This enhancement applies to Redwood Benefits pages only.

## 🔐 Access Requirements

The agents users can view depend on the roles and privileges assigned to them. To access the Benefits Analyst Agent, the user's role must be explicitly granted access to the agent by an AI Studio Administrator. See How can I give users access to AI agents and Access Requirements for AI Agent Studio.

Users must also have access to the existing Benefits Analyst Agent and the Redwood Benefits experience.

## 📚 Key Resources

• Explore AI Agents for Oracle Fusion Cloud Applications
• How do I use AI Agent Studio?
• How do I use Benefits AI Agents?
• How can I give users access to AI agents?
• Access Requirements for AI Agent Studio

---
*Oracle Cloud Readiness · 26C · HCM · Benefits*