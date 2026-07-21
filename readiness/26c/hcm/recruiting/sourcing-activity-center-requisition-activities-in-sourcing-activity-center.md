[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Recruiting](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/recruiting.md)

# Sourcing Activity Center: Requisition Activities in Sourcing Activity Center

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/recr-26c/26C-recruiting-wn-f46429.htm)

Requisitions is now available as an activity item type in the Sourcing Activity Center. Also available are Recruiter and Hiring Manager columns and Requisition and Hiring Manager filters.

The Recruiting activities available are the same as are found in the Recruiting Activity Center. They are:

• Approval rejected
• Waiting to be submitted
• Awaiting formatting
• Awaiting posting
• Pending approval
• No applications lately
• Expired career site posting
• Expired staffing agents invitations
• All openings filled

The activities you enable for requisitions will automatically appear in both the Recruiting Activity Center and the Sourcing Activity Center. Completing or dismissing an activity in one activity center will remove it from the list in both activity centers.

Requisition Activities on the Sourcing Activity Center

**Business benefit:**Increased visibility into the Candidate Sourcing product area of requisitions that require sourcing efforts.

## ⚙️ Steps to Enable and Configure

The Candidate Sourcing tile appears when these profile options are enabled:

• ORA_IRC_RECRUITING_REDWOOD_ENABLED
• ORA_IRC_ENABLE_RAC

For details, see How do I enable a profile option?

For details on how to configure activities in the Sourcing Activity Center, see How do I configure activities in the Sourcing Activity Center?

Users also need privileges to access the Candidate Sourcing tile. For details, see the **Access Requirements**section.

Users also need privileges to access the Candidate Sourcing tile, the Sourcing Activity Center, and Booster (for Events). For details, see the **Access Requirements**section.

## 🔐 Access Requirements

Users need the following combination of privileges or aggregate privileges to access the Sourcing Activity Center within Candidate Sourcing:

• Manage Recruitment Campaign (IRC_MANAGE_RECRUITMENT_CAMPAIGN)
• View Recruitment Campaign (IRC_VIEW_RECRUITMENT_CAMPAIGN)
• Manage Recruiting Event (ORA_IRC_MANAGE_RECRUITING_EVENT)
• View Recruiting Events (ORA_IRC_VIEW_RECRUITING_EVENT)
• Manage Candidate Pool (IRC_MANAGE_CANDIDATE_POOL)
• Search for Candidates (ORA_IRC_SEARCH_FOR_CANDIDATES)

Additionally, users need the privilege Access Sourcing Activity Center (IRC_ACCESS_SOURCING_ACTIVITY_CENTER) for the Sourcing Activity Center page to appear in the Candidate Sourcing area and for the Quick Action to appear.

To manage the KPI and Visualizations which can be displayed, users need the Edit Sourcing Activity Center Layout (IRC_EDIT_SOURCING_ACTIVITY_CENTER_LAYOUT) privilege.

---
*Oracle Cloud Readiness · 26C · HCM · Recruiting*