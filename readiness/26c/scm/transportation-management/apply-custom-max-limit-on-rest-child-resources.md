[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# Apply Custom Max Limit on REST Child Resources

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f47431.htm)

This Optional Feature, when enabled, allows you to define maximum thresholds for child resource records using system properties. Once set, these limits are automatically enforced whenever REST services return related child data. This ensures that only a manageable number of records are included in each response, improving efficiency without requiring changes to existing integrations.

You use this capability when integrating external systems, building custom applications, or managing high-volume transactional data through REST APIs. By limiting the volume of child data returned, you can maintain consistent performance and avoid overloading downstream systems.

**Business Benefit:** This feature helps to improve system performance and improve integration reliability by controlling data volume:

• Reduces response times for REST API calls
• Prevents excessive data transfer and system strain
• Improves stability for high-volume integrations
• Helps ensure consistent performance across environments

## ⚙️ Steps to Enable and Configure

If you need to change the Opt In state for this feature:

• Go to the Optional Feature UI - **Configuration and Administration > Property Management > Optional Features**.

Your user must have the DBA.ADMIN user role to use this functionality.

• Select the**Apply Custom Max Limit on REST Child Resources**feature.
• Run the desired Action for the feature - Opt In or Opt Out.

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*