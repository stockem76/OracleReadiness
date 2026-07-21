[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Product Lifecycle Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/product-lifecycle-management.md)

# Selected Product Management Bug Fixes In This Update

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/plm26c/26C-plm-wn-f49985.htm)

This update includes some bug fixes that can change the way Oracle Fusion Cloud Product Lifecycle Management works. This isn't a full list of all the bug fixes in this update. This list includes the bug fixes that can cause a noticeable change in application behavior.

**Display Object Name and Description for Clipboard and Spotlight Objects**

Before update 26C, the object name and description wasn't displayed for the Clipboard and Spotlight objects. After update 26C, when you hover over objects within Clipboard and Spotlight, the corresponding object name and description is displayed.

Oracle reference: 39000480

**Links to Project Tasks on Item and Workflow Relationships**

Before update 26C, you couldn’t add a Project Task in the Links section of the Relationships tab for an item or a workflow on Redwood pages. After update 26C, you can add a Project Task from the Relationships tab.

Oracle reference: 39410123

**Use Filters in Where Used Data**

Before update 26C, you were unable to use the filters on columns appearing in the Where Used data for an item. After update 26C, you can use the filters.

Oracle reference: 39116879

**Retrieve Details Using Workflow Policy Advisor**

Before update 26C, the tool for retrieving workflow details wasn’t retrieving the correct information. After update 26C, the issue is fixed. Additionally, you can also ask questions about affected object lines and other change orders when the change number is mentioned in single or double quotes. For more information, refer to AI Agent: Workflow Policy Advisor.

Oracle reference: 39332192

**Access All Workflows on Supplier Portal Using Links in Notifications**

Before update 26C, clicking the workflow objects (change orders, change requests, problem reports, and corrective actions) hyperlink in the notification opened in the supplier portal in the classic interface, although the Redwood page was enabled. After update 26C, clicking the change order hyperlink in the notification will take you to the object in the supplier portal on the Redwood page. It will take you to the classic page if the Redwood page is disabled.

Oracle reference: 39185291

**Search for Workflow Approval from Supplier Portal**

Before update 26C, you were unable to search for workflow approvals from the supplier portal. After update 26C, you can search for workflow approvals from the supplier portal.

Oracle reference: 39185301

**Data Presence Indicators for Quality Objects**

Data Presence Indicators for Quality Objects

  Before Update 26C, a row for data presence indicators was created in the database for quality issues and actions, problem reports, and corrective actions, even when the indicators were disabled (set to False). This behavior occurred for objects in both the reference and definition organizations.

  Starting with Update 26C, a Data Presence Indicators row is created only when the indicators are enabled (set to True). Additionally, when the indicators are enabled, a corresponding row is created in a new database table. This behavior is now consistently applied across both the reference and definition organizations.

Oracle reference: 39160448

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · SCM · Product Lifecycle Management*