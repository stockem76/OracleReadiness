[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Risk Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/risk-management.md)

# Agentic AI App: Security Command Center

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/risk26c/26C-risk-wn-f49543.htm)

This AI application continuously analyzes risk data from Oracle Risk Management Cloud to identify problematic roles, users, and transactions. The application provides prioritized recommendations, targeted remediation steps, and communication workflows to help security analysts and administrators to take action, sustain compliance, and improve access governance.

Security Command Center includes the following panels:

• An "Ask Oracle" search bar to ask relevant questions about the risks in your business processes
• Summary panel that displays an AI generated summary of the most pressing access risks and relevant transactions in your business processes
• *Top 5 Roles with Intra-role* *Violations*panel displays the roles with the most number of inherent separation of duties (SoD) violations and users assigned to them
• *Top 5 Users with Access Violations* panel displays the users with the most access violations
• *Transaction Activity* panel displays the top 10 users with high risk transaction violations based on their assigned access
• *Business Process Compliance* panel displays the overall compliance health by business process
• Prioritized actions panel analyzes high-risk user access and allows reviewers to revoke offending roles from users
• Communications panel enables sharing of access analysis details with stakeholders, including recommendations to remediate intra-role violations for high-risk roles and compliance summaries by process

**Note:** This application is offered under Controlled Availability. Do not use it in production until it becomes generally available. Use the application in non-production environments only.

## 🎯 Business Benefit

This Agentic AI application enables security administrators and analysts to continuously monitor security. The application provides visibility into high-risk access and transaction violations and role design issues, and enables these stakeholders to take action using AI-generated recommendations and prioritized actions.

## ⚙️ Steps to Enable and Configure

• As an AI Studio administrator with access to Advanced Controls REST service, navigate to AI Agent Studio (see Access Requirements section).
• Next, navigate to the Agent Teams tab and edit and run these AI Agents from the list of Published agent teams in the given sequence. Wait for each agent team to complete before proceeding to the next one. These AI Agents generate the summarized data used by the Security Command Center AI application:

1. RMC Data Stores Generation Assistant
2. RMC IntraRole Violations Generator
3. RMC Role Recommendations Generator
4. RMC User Access Violations Generator
5. RMC Transaction Violations Generator
6. RMC Business Process Compliance Generator

• To run these agent teams, use any user prompt such as "Generate Data".
• After an initial run, invoke the *Security Command Center* by navigating to the '*Apps*' tab of AI Agent Studio.
• While the *RMC Data Stores Generation Assistant* agent team needs to be run only once, you can schedule the other 5 agent teams to run on a schedule in the same sequence as mentioned above. Each of these agent teams will ingest the latest access and transaction control analysis results and generate summarized insights that will be used by the Security Command Center app.

## 🔐 Access Requirements

• Create an AI Agent Studio Admin job role and assign it to an AI Admin user. Follow these steps to configure this job role:

1. In Security Console, create a new custom job role with Role Category 'GRC - Job Roles'. Make sure to enable permission groups for this job role.
2. On the *Functional Security Policies* page, add privilege *Access Intelligent Agent Chat* (HRC_ACCESS_AI_AGENT_CHAT_PRIV)
3. On the *Role Hierarchy* page, open the Roles and Privileges tab and add these roles:
• *Manage Risk Intelligent Agent* (ORA_GTG_MANAGE_RISK_AI_AGENT_DUTY)
• *Manage Risk Intelligent Agent* (ORA_GTG_MANAGE_RISK_AI_AGENT_DUTY_HCM)
4. Open the *Roles and Permission Groups* tab and add the following duties:
• *Fai Genai Agent GRC Administrator Duty* (ORA_DR_FAI_GENERATIVE_AI_AGENT_GRC_ADMINISTRATOR_DUTY)
• *Fai Genai Manager Duty* (ORA_DR_FAI_GENERATIVE_AI_MANAGER_DUTY)
• *Fai Genai Agent Runtime Duty* (ORA_DR_FAI_GENERATIVE_AI_AGENT_RUNTIME_DUTY)
5. Save the custom role and assign this custom role to the admin user

• To enable permission groups for roles: 
  • In the Setup and Maintenance work area, search for the **Manage Administrator Profile Values** task using the search link in the Tasks panel tab.
• Search for the Enable Security Console External Application Integration (ORA_ASE_SAS_INTEGRATION_ENABLED) profile option and set the Site profile level to **Ye****s**.
• Assign the following role to the AI Admin user who will be configuring the Security Command Center App: 
  • *Manage Advanced Controls REST Services* (ORA_GTG_MANAGE_ADVANCED_CONTROLS_REST_SERVICES_DUTY)

## 📚 Key Resources

• Oracle AI For Fusion Applications
• Overview of Agentic Apps

---
*Oracle Cloud Readiness · 26C · ERP · Risk Management*