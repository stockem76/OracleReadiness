[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Global Trade Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/global-trade-management.md)

# Enable Friendly XML Schema Validation Messages

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/gtm26c/26C-gtm-wn-f49483.htm)

This Optional Feature, when enabled, provides readable and user-friendly XML validation error messages by converting complex, system-generated errors into simpler, more understandable explanations. This enhancement helps both business users and administrators troubleshoot validation failures more efficiently. By making validation feedback easier to understand, the feature reduces dependency on technical support teams and accelerates issue resolution during day-to-day operations.

**Business Benefit:** This feature helps you resolve XML validation issues more quickly and with less technical expertise.

Key business benefits include:

• Reduced time spent troubleshooting XML validation failures
• Improved user experience through clearer and more actionable error messages
• Fewer support escalations to technical teams
• Faster correction and resubmission of failed transactions
• Improved operational efficiency for integration and data management processes

## ⚙️ Steps to Enable and Configure

If you need to change the Opt In state for this feature:

• Go to the Optional Feature UI - **Configuration and Administration > Property Management > Optional Features**.

Your user must have the DBA.ADMIN user role to use this functionality.

• Select the**Enable Friendly XML Schema Validation Messages**feature.
• Run the desired Action for the feature - Opt In or Opt Out.

## 💡 Tips and Considerations

• The feature simplifies validation messages but does not change the underlying XML validation rules.
• You should still ensure that XML documents conform to the required schema and formatting standards.
• Simplified messages are intended to help identify the issue more quickly, but complex integration problems may still require administrator or technical review.
• Error messages may vary depending on the type of XML validation failure encountered.
• This enhancement improves readability and troubleshooting efficiency but does not automatically correct invalid XML content.

---
*Oracle Cloud Readiness · 26C · SCM · Global Trade Management*