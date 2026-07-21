[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Oracle Fusion Field Service](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/oracle-fusion-field-service.md)

# Extend Project-Based Work with Project and Task Fields in Forms

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/fscv-26c/26C-fsvc-wn-f49357.htm)

**Note**

  This enhancement only applies to Oracle Fusion Field Service environments. You can verify whether you've Oracle Field Service or Oracle Fusion Field Service, by signing in and checking on the **About** page.

Oracle Fusion Field Service introduced native interaction with Fusion Project Management in Update 25D. With update 26C, administrators can extend that project context into Oracle Fusion Field Service forms by adding supported Project and Project Task fields to the forms used during field work implementation. Project fields are available as read-only fields in forms. Supported Project Task fields can also be added to forms. Most Project Task fields are read-only, while Task Name and Task Description are read-write. Supported Project Task descriptive flexfields (DFFs) can also be added to forms as read-write fields.

For example, a mobile worker working on a project-based installation can open a Field Service form and review the related project name, project description, task number, task dates, and task level before completing the work. If the task name or task description needs to be updated, the mobile worker can update directly in the form. This helps customers bring project-specific information into the forms that support project-driven field activities.

## ⚙️ Steps to Enable and Configure

1. Navigate to the **Forms & Plugins** page.
2. Create a form or open an existing form.
3. Add the supported Project or Project Task fields to the form.
4. Configure the fields according to the supported form behavior.
5. Publish the form.
6. Open an activity related to a Project or Project Task and verify that the fields display as expected.

## 💡 Tips and Considerations

• Project fields are read-only in forms.
• Task Name and Task Description are read-write in forms.
• Other supported Project Task fields are read-only.
• Supported Project Task descriptive flexfields (DFFs) are read-write in forms.
• Review existing forms, training materials, and project-based work processes to decide where project information should be shown.
• Review the native interaction between Oracle Fusion Field Service and Fusion Project Management introduced in Update 25D to understand how field activities can be associated with project tasks.

## 📚 Key Resources

• Native interaction between Fusion Field Service and Fusion Project Management

## Supported Fields

### Project Fields

The following Project fields are available in Oracle Fusion Field Service forms.

Project Fields

Field | Form Behavior
Project ID | Read-only
Project Name | Read-only
Project Description | Read-only

### Project Task Fields

The following Project Task fields can be shown for an activity in Oracle Fusion Field Service forms.

Project Task Fields

Field | Form Behavior
Project Element ID | Read-only
Task Number | Read-only
Task Name | Read-write
Task Description | Read-write
Task Start Date | Read-only
Task Finish Date | Read-only
Task Level | Read-only

### Project Task Descriptive Flexfields

The following Project Task descriptive flexfield types can be added to forms as read-write fields:

Project Task Descriptive Flexfields

Descriptive Flexfield Type | Form Behavior
Text | Read-write
Number | Read-write
Datetime | Read-write

**Business Benefits**

• Extends project-based work support by making supported Project and Project Task information available in Oracle Fusion Field Service forms.
• Reduces duplicate data entry by using supported project information instead of separate custom fields.
• Improves data consistency by using information from related Project and Project Task records.

---
*Oracle Cloud Readiness · 26C · SERVICE · Oracle Fusion Field Service*