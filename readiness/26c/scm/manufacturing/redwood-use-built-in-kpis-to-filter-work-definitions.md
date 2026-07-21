[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Manufacturing](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/manufacturing.md)

# Redwood: Use Built-in KPIs to Filter Work Definitions

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/mfg26c/26C-mfg-wn-f44522.htm)

Currently, the list of work definitions on the Work Definition Overview page is static. It displays all work definitions in the manufacturing plant. With this update, the list of work definitions displayed is based on the selected KPI. The following KPIs are available on the Work Definition Overview page:

• New Work Definitions - Past 30 Days.
• Updated Work Definitions - Past 30 Days.
• Work Definitions with Structure Changes - Next 30 Days.
• Draft Work Definitions - When electronic signatures are enabled for work definitions in the plant.
• Pending Approval Work Definitions - When electronic signatures are enabled for work definitions in the plant.

KPI: New Work Definitions Created in the Past 30 Days

KPI: Work Definitions Updated in the Past 30 Days

KPI: Work Definitions with Structure Changes in the Next 30 Days

Replacing a static list of work definitions with a dynamic KPI-driven view that surfaces the relevant items in real time enables users to focus on what needs their attention. Actionable KPIs eliminate manual filtering and enhance the user experience.

## ⚙️ Steps to Enable and Configure

Use the following steps to enable or disable this feature:

1. In the Setup and Maintenance work area, search for and select the **Manage Administrator Profile Values** task.

1. On the Manage Administrator Profile Values page, search for and select the **ORA_WIS_WORK_DEFINITION_LANDING_PAGE_REDWOOD_ENABLED** profile option code.

1. In the Profile Values section, set the Site level to **Y**or **N**. The default value of the profile option is N.

• Y = enables the feature
• N = disables the feature

1. Click **Save and Close**. Changes in the profile value will affect users the next time they sign in.

Profile Option to Enable the Work Definition Landing Page with the Redwood User Experience

## 💡 Tips and Considerations

• The count of work definitions on the KPI is based on the work definition header whereas the count of work definitions in the search results table is based on work definition versions. Therefore, there may be cases where the count in the search results table is greater than the count on the KPI.
• The Draft Work Definitions and Pending Approval Work Definitions KPIs are shown when electronic signatures are enabled for work definitions in the plant.
• Use the Redwood Work Definitions page for additional filters and keyword search. Refer to the 24B feature "Search for, Create, and Edit a Standard Item Work Definition Using the Redwood User Experience".

## 🔐 Access Requirements

Users who are assigned a configured job role that contains this privilege can use this feature:

• Manage Work Definition Work Area (WIS_MANAGE_WORK_DEFINITION_WORK_AREA_PRIV)

This privilege was available prior to this update.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: Refer to the Using Manufacturing guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Refer to the Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Manufacturing*