[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [HCM Common](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/hcm-common.md)

# Redwood Experience for HCM Extracts

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hcom26c/26C-hcm-common-wn-f49704.htm)

Enrich the user experience with the new **Extract Configuration Group**page developed using the Redwood toolset. Built from the ground up with Visual Builder Studio (VBS), this page delivers a distinctive and modern Oracle applications experience.

The redesigned landing page enables you to quickly search and manage extract configuration groups from a centralized interface.

You can view seeded and custom extract configuration groups listed with related information including the name, code, description, and last updated date.

### Search for Extract Configuration Groups

Use the search field at the top of the page to search for extract configuration groups by name. The results are dynamically filtered based on your search criteria, making it easier to locate configuration groups in environments with large numbers of records.

### Import Extract Configuration Groups

Use the Import action to import extract configuration group XML files directly from the landing page. The import panel supports drag-and-drop or file selection for uploading configuration group files.

If an imported configuration group already exists, you can choose whether to overwrite the existing configuration or retain it.

### Export Extract Configuration Groups

Use the Export action to export one or more user-created extract configuration groups as an XML file. The export panel allows you to select the required configuration groups for bulk export.

### Copy Extract Configuration Groups

Use the **Copy**action from the **Actions**menu for a selected record to create a new extract configuration group by reusing an existing configuration. You can provide a new name and description for the copied configuration group.

### Edit Parameter Values for an Extract Configuration Group

Click the extract configuration group name to review the default values for the attributes in the **Parameters**and **Features**tab and provide a new value to change the defaults.

### Delete Extract Configuration Groups

Use the **Delete**action from the **Actions**menu to remove an extract configuration group. A confirmation dialog is displayed before the configuration group is deleted.

**Business Benefit:** The **Extract Configuration Groups** page is now redesigned using the Redwood user experience to provide a modern, streamlined interface for managing extract configuration groups. The refreshed experience improves usability and navigation while retaining the existing functionality for creating, importing, exporting, copying, and deleting extract configuration groups.

## ⚙️ Steps to Enable and Configure

Here are the profile option details for Extract Configuration Group. By default, the extracts profile option is delivered as enabled (Yes).

Profile Option Code | Profile Option Display Name | Value
ORA_HCM_EXTRACT_CONFIGURATION_GROUP_REDWOOD_ENABLED | Enable Redwood Extract Configuration Groups | Yes

## 🔐 Access Requirements

The Extract Configuration Groups page is secured with the function security privilege: PER_MANAGE_HCM_EXTRACT_DEFINITION_PRIV

## 📚 Key Resources

For more information, see How do I enable a profile option?

---
*Oracle Cloud Readiness · 26C · HCM · HCM Common*