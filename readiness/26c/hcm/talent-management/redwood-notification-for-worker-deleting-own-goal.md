[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Redwood: Notification for Worker Deleting Own Goal

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f49992.htm)

Notify managers when team members delete performance or development goals that their team members created and ensure that the managers are informed of the changes in the priorities of the team members. This notification will help managers evaluate if the goal deletion is appropriate or not.

Notification to manager after a team member deletes a performance goal that they created

Notification to manager after a team member deletes a development goal that they created

This feature provides these benefits to line managers:

• Increased visibility to team members decisions
• Enhanced performance tracking and auditing
• Ability to understand the workload issues of team members

## ⚙️ Steps to Enable and Configure

To enable Redwood Goals Center, you need to enable the profile options indicated in the table.

Profile Option Code | Profile Option Display Name | Value
ORA_HCM_VBCS_PWA_ENABLED | Enable VBCS Progressive Web Application User Interface | Y
ORA_HRA_PERFORMANCE_DOCUMENTS_AND_GOALS_REDWOOD_ENABLED | Enable Redwood Performance Documents and Goals Center | Yes

**NOTE**: The Performance Document, Check-in, and Goals Center features are closely connected. So, the Redwood version of these pages can all be enabled or disabled only using the common ORA_HRA_PERFORMANCE_DOCUMENTS_AND_GOALS_REDWOOD_ENABLED profile option. These features can't be enabled individually.

For more information, see How do I enable a profile option?.

To enable Redwood notifications for deletion of own performance and development goals to managers, do these steps:

1. Use the **Alerts Composer** tool.
2. Search for the **Performance Goals** **Alerts** event.
3. Ensure that the **Manager Notified After Worker Deletes Goal** alert is enabled.
4. Search for the **Development Goals Alerts** event.
5. Ensure that the **Manager Notified After Worker Deletes Goal** alert is enabled.

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*