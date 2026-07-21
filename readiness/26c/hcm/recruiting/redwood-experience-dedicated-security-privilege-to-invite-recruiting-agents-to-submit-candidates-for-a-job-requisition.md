[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Recruiting](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/recruiting.md)

# Redwood Experience: Dedicated Security Privilege to Invite Recruiting Agents to Submit Candidates for a Job Requisition

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/recr-26c/26C-recruiting-wn-f49666.htm)

You can control who can invite recruiting agents to submit candidates for a job requisition using a new security privilege: **Post Job Requisition to Recruiting Agents.**

Previously, the ability to invite recruiting agents from a job requisition was tied to the broader security privilege **Access to Hiring as Recruiter**. Because that privilege was designed to provide recruiter-level access, customers often had to grant more access than necessary when they wanted hiring managers to invite recruiting agents.

With this update, administrators can grant a more targeted privilege only to the roles that need the ability to invite recruiting agents. Users with the new privilege can open a job requisition, navigate to the Posting tab, and use the Invite Agents section to invite recruiting agents. Users without the privilege won’t see the Invite Agents section and won’t be able to invite agents.

**Business benefit:**This enhancement gives customers a more precise and secure way to manage recruiting-agent invitations. Administrators can allow hiring managers to invite recruiting agents without granting broader recruiter access, helping align agent posting with the more granular security model used for other posting actions.

## ⚙️ Steps to Enable and Configure

See the **Access Requirements** section.

To use Redwood experience, you need to enable the Recruiting Redwood pages profile options. For details, see Set profile options for Redwood pages.

For details on enabling and customizing Redwood for HCM, see How do I adopt Redwood for HCM? and Extending Redwood Applications for HCM and SCM Using Visual Builder Studio

## 💡 Tips and Considerations

If users can’t see the Invite Agents section, confirm that:

• Their role includes the new privilege
• They have access to the requisition and posting flow

## 🔐 Access Requirements

To allow a role to invite recruiting agents to submit candidates for a job requisition, add the following function security privilege to the role:

• Post Job Requisition to Recruiting Agents (IRC_POST_JOB_REQUISITION_TO_RECRUITING_AGENTS_PRIV)

Once the updated role is available, users can navigate to Hiring > Requisitions > Posting tab and use the Invite Agents section to invite recruiting agents.

**Note:** The seeded Hiring Manager role doesn’t include this new privilege. Hiring managers must be assigned a custom role that includes the privilege before they can access the Invite Agents section.

This privilege secures all recruiting-agent posting tasks, including selecting agents and managing posting expiration dates.

---
*Oracle Cloud Readiness · 26C · HCM · Recruiting*