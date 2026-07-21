[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Redwood: Enable Mass Actions for Development Goals from Goals Center

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f49467.htm)

From this release, as administrators you can enable workers, managers, and HR specialists to select multiple development goals and act upon them.

Employees can share, delete, or make the selected goals inactive on their Goals Center. If they are managers, then they can also assign their goals.

Actions for Multiple Selected Development Goals for a Manager when viewing their goals

Actions for multiple selected development goals for an employee

Managers can now delete or make the selected goals inactive when they access the team member’s Goals page from their Team Goals Center.

Actions for multiple selected development goals of a team member for a manager

HR specialists can delete or make the development goals that they select for a person inactive.

Actions for multiple selected development goals of others for an HR specialist

Validations are done for all the development goals that are selected. The actions are enabled for the multiple selected goals only if all the selected goals pass the validation test and if the user has the privilege to do the action. For more information on this, see Why are some actions disabled for development goals? .

The business rule configurations done for the goal actions in Visual Builder Studio also apply. If some actions are hidden for a specific role, then the person with that role won’t be able to perform the mass action.

## 🎯 Business Benefit

Increase the ease of managing goals by enabling workers, managers, and HR specialists to select multiple development goals to act on them.

## ⚙️ Steps to Enable and Configure

To enable Redwood Goals Center, you need to enable the profile options indicated in the table.

Profile Option Code | Profile Option Display Name | Value
ORA_HCM_VBCS_PWA_ENABLED | Enable VBCS Progressive Web Application User Interface | Y
ORA_HRA_PERFORMANCE_DOCUMENTS_AND_GOALS_REDWOOD_ENABLED | Enable Redwood Performance Documents and Goals Center | Yes

**NOTE**: The Performance Document, Check-in, and Goals Center features are closely connected. So, the Redwood version of these pages can all be enabled or disabled only using the common ORA_HRA_PERFORMANCE_DOCUMENTS_AND_GOALS_REDWOOD_ENABLED profile option. These features can't be enabled individually.

For more information, see How do I enable a profile option?.

For information about the privileges that need to be granted to the role of employees, managers, and HR specialists to allow to perform the action, see Privileges to Secure Goal Actions.

Ensure that the actions aren’t hidden by configuring rules in Visual Builder Studio. For more information on how to do this, see How do I hide or show a field in Visual Builder Studio?

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*