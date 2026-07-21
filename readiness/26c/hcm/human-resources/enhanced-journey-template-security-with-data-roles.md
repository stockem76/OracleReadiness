[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Human Resources](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/human-resources.md)

# Enhanced Journey Template Security with Data Roles

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hure-26c/26C-hr-wn-f44451.htm)

The enhanced journey template security now uses the `rolesLOV` REST resource to display existing roles when you configure journey template security. The Role list returns assignable roles only, and the available role types include job, abstract, and data roles. This makes role selection more focused and consistent when you set up journey template security.

Administrators can search and select only roles that can be assigned and don’t need to filter through non-assignable options during setup. This helps reduce configuration errors and makes security setup faster and more accurate. By displaying the relevant role types in one list of values, the experience is easier to use.

Role List on Journey Security UI Displaying Job Roles

Role List on Journey Security UI Displaying Abstract Roles

Role List on Journey Security UI Displaying Data Roles

This feature improves the efficiency, accuracy, and usability of journey template security configuration by showing administrators only valid, assignable roles in a unified role selection list.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 🔐 Access Requirements

You must be granted the Manage Journey (ORA_PER_MANAGE_JOURNEY_TEMPLATE) aggregate privilege to work on journey templates.

## 📚 Key Resources

For more information, refer to the Implementing and Using Journeys guide.

---
*Oracle Cloud Readiness · 26C · HCM · Human Resources*