[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# Deprecate Basic Auth for BIP SOAP Web Service

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f47435.htm)

This Optional Feature, when enabled, will deprecate the report generation and delivery processes that previously relied on username and password authentication. Instead, you are required to use an OAuth-based authentication through the **“BI Publisher SOAP with OAuth”** report system type. .

See the feature OAuth Authentication for BI Publisher SOAP Report Services for more information. This ensures that integrations leverage secure token-based access rather than static credentials.

This feature improves security and aligns with modern authentication standards, support for using basic authentication (user credentials) with BI Publisher SOAP web services has been deprecated. This change addresses the risks associated with transmitting and managing user credentials directly in integrations, which can expose sensitive information and increase vulnerability to unauthorized access.

**Business Benefit:** This feature improves security and reduces risks by eliminating less secure authentication methods.

• Protects sensitive credentials by replacing them with secure token-based authentication
• Reduces the risk of unauthorized access and credential exposure
• Aligns your reporting integrations with modern security and compliance standards
• Supports more scalable and maintainable integration practices

## ⚙️ Steps to Enable and Configure

You will need to review existing BI Publisher SOAP integrations that use username and password authentication and update the report configurations to use the **“BI Publisher SOAP with OAuth”** report system type.

If you need to change the Opt In state for this feature:

• Go to the Optional Feature UI - **Configuration and Administration > Property Management > Optional Features**.

Your user must have the DBA.ADMIN user role to use this functionality.

• Select the**Deprecate Basic Auth for BIP SOAP Web Service**feature.
• Run the desired Action for the feature - Opt In or Opt Out.

## 💡 Tips and Considerations

See the feature OAuth Authentication for BI Publisher SOAP Report Services for more information.

**Note:** If are currently using a report generation and delivery processes that relies on username and password authentication, you will need to move to an OAuth-based authentication through the **“BI Publisher SOAP with OAuth”** report system type before Deprecate Basic Auth for BIP SOAP Web Service expiration.

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*