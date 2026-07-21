[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Help Desk](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/help-desk.md)

# REMINDER: Migrate from Classic HR Help Desk to Redwood prior to 27A

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/shde-26c/26C-helpdesk-wn-f47355.htm)

Classic HR Help Desk is now deprecated, and all organizations must migrate to Help Desk in the Redwood experience prior to their 27A update.

HR Help Desk in the Redwood Experience provides a modern user interface and makes the employee experience consistent with the HCM Redwood experience. It also provides many new features that are not found in Classic HR Help Desk, such as AI Assistance, Chat, Case Management, Journeys Integration, Internal Help Desk, and many other features that have been released or are planned.

## ⚙️ Steps to Enable and Configure

Steps to enable the Migration tools are found in the **Migration Guide**, available through Classic HR Help Desk Migration Resources on Cloud Customer Connect.

## 💡 Tips and Considerations

Our recommendation is to:

• Work along with the videos, pausing if you need additional time to do the steps.
• Follow along in the documentation and workbook to make it easy to cut-and-paste name, codes, or XML.
• Make certain that all validation steps are completed successfully before moving to the next step.
• If you encounter an error with no resolution given, open a Service Request with Technical Support to resolve the issue before continuing.

## 🔐 Access Requirements

To begin setup, you must be logged in with an account that has the following privileges and/or Roles:

• **Application Implementation Consultant Resource** (ORA_HZ_RESOURCE_ABSTRACT)
• **Next Gen Human Resource Help Desk Administrator**Job Role (ORA_SVC_HUMAN_RESOURCE_HELP_DESK_ADMINISTRATOR_NG)
• **Human Resource Help Desk Administrator**Job Role (ORA_SVC_HUMAN_RESOURCE_HELP_DESK_ADMINISTRATOR)
• **HR Service Request Administration** Duty Role (ORA_SVC_HR_SR_ADMINISTRATION)
• **HR Help Desk Administration** Duty Role (ORA_SVC_HELPDESK_ADMINISTRATION)
• **Delete HR Service Request**Function (SVC_DELETE_HR_SR) (given to ADMINISTRATION Job Role OOTB)
• **Schedule Internal Help Desk Jobs** Privilege (SVC_SCHEDULE_SERVICE_JOBS) (given to ADMINISTRATION Job Role OOTB)

## 📚 Key Resources

Migration resources are found on Cloud Customer Connect at: Classic HR Help Desk Migration Resources.

Start by watching the Migration Kick-off video and then follow along as the videos, following along with the documentation, to guide you through the data migration.

These documents will help on your migration Journey:

1. **Migration Guide** (PDF) - Step-by-step instructions on how to use the migration tools and what to consider along the way.
2. **Migration Workbook** (XLS) - A place to keep notes, results of reports, queries, test references, etc.
3. **Migration Checklist** (Word) - A companion to the Migration Guide, this allows you to check off each major step as you complete each task. You can also add your own tasks or remove tasks that are not applicable, since this is an editable document.

---
*Oracle Cloud Readiness · 26C · SERVICE · Help Desk*