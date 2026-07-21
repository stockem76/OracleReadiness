[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Compensation](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/compensation.md)

# Enhancements to Redwood Salary, Compensation History Extensibility

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/comp-26c/26C-compensation-wn-f43712.htm)

You can now configure decimal settings for monetary values in the Redwood View Compensation History summary page. In addition, enhancements to defaulting and validation allow you to apply both rules to the same field and leverage job, assignment EFF for more dynamic business rules.

View Compensation History with Configured Monetary Display

Decimal Setting Page Properties Configured for Salary, Other Compensation and Recurring Payments Group

Define Defaulting and Validations using Job and Assignment EFF

These updates improve configurability, data consistency, and policy enforcement across Redwood compensation flows.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

1. Decimal settings affect monetary values only.
2. For assignment or job EFF-based defaulting and validation to work, users must have read-only access to the relevant EFF data through appropriate security privileges. For example Matt is a line manager. Their organization has setup a defaulting rule that looks for assignment EFF and defaults the salary basis. Matt's security needs to provide them read access to the assignment EFF for the defaulting to work when Matt is performing the salary change.

## 🔐 Access Requirements

Below are the security requirements the logged-in user must have for defaulting and validations that rely on assignment and job EFF to function correctly:

Name | Code | Purpose | Type
Read HR Job Business Object | PER_READ_HR_JOB_BO | For the logged in user to access job EFF details | Function Security
Read Worker Assignment Business Object | PER_READ_WORKER_ASSIGNMENT_BO | For the logged in user to access assignment EFF details | Aggregate Privilege

## 📚 Key Resources

Also see 26A Feature: Business Rule Defaulting and Validation of Input Values Introduction

For more information about compensation business rules, see these playbooks:

• How do I configure business rules for Redwood individual compensation pages?
• How do I configure business rules for Redwood salary pages?
• Which are the business objects and privileges securing them for defaulting and validation rules?

---
*Oracle Cloud Readiness · 26C · HCM · Compensation*