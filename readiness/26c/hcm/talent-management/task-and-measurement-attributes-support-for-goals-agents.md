[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Task and Measurement Attributes Support for Goals Agents

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f49464.htm)

From this release, when you use the **Employee Goals Assistant** or the **Team Goals Assistant** AI workflow agents, you can query or update these additional task attributes for performance and development goals:

• Name
• Description
• Task type
• Start date
• Target completion date
• Task priority
• Comments
• Related link
• Unit of measurement
• Target type
• Target value
• Actual value
• Achieved weight
• Completion status
• Actual completion date
• Minimum target
• Maximum target
• Target percentage

You can query or update these measurement attributes of performance and development goals:

• Unit of measurement
• Target type
• Target value
• Target percentage
• Minimum target
• Maximum target
• Actual value
• Achieved weight

You can query or update these additional attributes of performance goals:

• Privacy status for employee goals
• Category
• Weight
• Actual completion date
• Comments
• Success criteria
• Related link
• Long description
• Goal sub type
• Level

You can query or update these additional attributes of development goals:

• Privacy status for employee goals
• Category
• Actual completion date
• Level
• Comments
• Success criteria

Use the **Employee Goals Assistant** and the **Team Goals Assistant** AI workflow agents effectively to get complete information and update more details of performance and development goals.

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

To learn how to create AI workflow agents, see Create Custom AI Agents of Type Workflow.

Create a guided journey task for the **Employee Goals Assistant** and the **Team Goals Assistant** AI workflow agents. For more information, see Configure Agent Task Type in Journeys. Note the guided journey code and add it to the guide journey page property of the page from which you want to invoke the **Employee Goals Assistant** or the **Team Goals Assistant** AI workflow agent. For example, on an employee’s Goals Center page you can add the guided journey code to the **Set Guided Journeys Code at the Page Level** page property. For more information, see Extend Application Page with Agent Guided Journey.

## 🔐 Access Requirements

The agents you can view depend on the roles and privileges assigned to you. To access this agent, your role must be explicitly granted access to it by an AI Studio Administrator. For more information, see How can I give users access to AI agents and Access Requirements for AI Agent Studio.

## 📚 Key Resources

• Explore AI Agents for Oracle Fusion Cloud Applications
• How do I use AI Agent Studio?

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*