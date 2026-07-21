[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Redwood: Restrict Matrix Manager Access to Goals

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f49991.htm)

From this release, as administrators, you can ensure that matrix managers can view only the performance or development goals that they created for a dotted-line report.

  After you enable this restriction, matrix managers can’t view performance or development goals created by others for the dotted-line report. But line managers can view all  the goals assigned to the person who’s their direct report, including the goals created by the matrix manager. Line managers can perform any actions they have permission for on goals created by matrix managers, just as they can on goals they created for their direct reports.

Performance goals of a dotted-line report seen by their matrix manager

Performance goals of a direct report seen by their line manager

Development goals of a dotted-line report seen by their matrix manager

Development goals of a direct report seen by their line manager

## 🎯 Business Benefit

Allow matrix managers to view only the goals that they created and ensure that they have only the information that they need to know.

## ⚙️ Steps to Enable and Configure

To enable Redwood Goals Center, you need to enable the profile options indicated in the table.

Profile Option Code | Profile Option Display Name | Value
ORA_HCM_VBCS_PWA_ENABLED | Enable VBCS Progressive Web Application User Interface | Y
ORA_HRA_PERFORMANCE_DOCUMENTS_AND_GOALS_REDWOOD_ENABLED | Enable Redwood Performance Documents and Goals Center | Yes

**NOTE**: The Performance Document, Check-in, and Goals Center features are closely connected. So, the Redwood version of these pages can all be enabled or disabled only using the common ORA_HRA_PERFORMANCE_DOCUMENTS_AND_GOALS_REDWOOD_ENABLED profile option. These features can't be enabled individually.

For more information, see How do I enable a profile option?.

Edit the Team Goals Center page and the Goals page of an employee in Visual Builder Studio and set the page properties to **true**.

• Show Only Development Goals Created by Matrix Managers
• Show Only Performance Goals Created by Matrix Managers

For more information on how to do this, see How do I control the display of a UI element in Visual Builder Studio?.

## 📚 Key Resources

For more information on extending Redwood pages in HCM, refer to this guide on the Oracle Help Center:

• Extending Redwood Applications for HCM and SCM Using Visual Builder Studio

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*