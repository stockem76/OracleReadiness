[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Recruiting](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/recruiting.md)

# Activity Centers: Initiate Sourcing Efforts Using AI Agent

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/recr-26c/26C-recruiting-wn-f46559.htm)

Use an AI Agent to initiate sourcing efforts when requisition activities in the Activity Center are generated. This agent is built specifically to be deployed into recruiting activities in the Activity Center.

Here's how it works:

A new agent template is available in AI Agent Studio: **Recruiting Sourcing Activity Center Agent Template**.

The **Recruiting Sourcing Activity Center Agent**works with the Activity Centers to automate recruiting activities such as creating candidate pools or creating campaigns. When the code of this agent is entered into the **Agent Team Code** field in a requisition activity and that activity gets assigned, this agent is invoked after the **Trigger Workflow Agents for Activity Items** scheduled process is run.

The following recruiting activities invoke the agent and the agent will create a campaign, a candidate pool or both depending on your configuration:

Agent creates a candidate pool for:

• Waiting to be submitted
• Awaiting formatting
• Awaiting posting
• Awaiting approval

Agent creates a campaign for:

• No applications lately

**Business benefit:**Enhances productivity by automatically enabling candidate sourcing activities such as creating campaigns or candidate pools.

## ⚙️ Steps to Enable and Configure

For information on entering the agent code and running the ESS job, refer to Automatically Launch AI Agent from Activities

## 💡 Tips and Considerations

The agent is only invoked for requisitions that are not in *draft* phase and that's state is *not posted*.

## 🔐 Access Requirements

Users need these privileges:

• View Job Requisition (IRC_VIEW_JOB_REQUISITION_PRIV)
• Manage Candidate Pool (IRC_MANAGE_CANDIDATE_POOL_PRIV)
• Manage Recruitment Campaign (IRC_MANAGE_RECRUITMENT_CAMPAIGN_PRIV)

## 📚 Key Resources

• Create AI Agents Using Preconfigured Agent Team Templates
• Explore AI Agents for Oracle Fusion Cloud Applications
• How do I use AI Agent Studio?
• How can I give users access to AI agents
• Access Requirements for AI Agent Studio

---
*Oracle Cloud Readiness · 26C · HCM · Recruiting*