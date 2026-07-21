[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Global Trade Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/global-trade-management.md)

# OAuth Authentication for BI Publisher SOAP Report Services

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/gtm26c/26C-gtm-wn-f49400.htm)

This feature provides you with the option to use OAuth 2.0 authentication for BI Publisher SOAP-based report generation and delivery services. This enhancement helps you modernize report integrations by replacing embedded BI Publisher user credentials with secure bearer-token authentication.

Previously, SOAP integrations required you to include BI Publisher usernames and passwords directly in requests. This created additional security and credential management challenges. With this update, you can configure a new report system type that uses OAuth 2.0 with JWT-based token generation for SOAP requests. The application retrieves a bearer token from a configured external authentication system and uses that token to securely authenticate report execution and printing requests. This allows you to continue using existing SOAP-based reporting workflows while aligning with enterprise security practices and cloud authentication standards.

**Business Benefit:**This feature helps you improve the security and maintainability of BI Publisher integrations by reducing reliance on embedded user credentials in SOAP requests.

Key benefits include:

• Improves security by using OAuth bearer tokens instead of storing or transmitting passwords
• Supports enterprise authentication standards and cloud security initiatives
• Allows you to continue using SOAP-based printing and delivery workflows that do not yet have REST equivalents
• Reduces operational risk associated with credential rotation and password management
• Enables phased adoption because you can use OAuth-based and existing basic-authentication integrations side by side

## ⚙️ Steps to Enable and Configure

1. Navigate to the Report System configuration area in your application.
2. Create a new report system or update an existing one.
3. Select the report system type: 
  • **BI Publisher SOAP Web Service with OAuth**
4. Configure the BI Publisher service endpoint details required for your environment.
5. Configure an External System that can generate OAuth bearer tokens using your organization’s authentication framework.
6. Associate the External System with the report system configuration.
7. Save the configuration.
8. Test document generation or printing workflows to confirm successful token generation and report execution.

## 💡 Tips and Considerations

• See the Optional Features Deprecate Basic Auth for BIP SOAP Web Service
• This feature is intended for SOAP-based BI Publisher integrations that still require capabilities not currently available through REST APIs, such as report printing and delivery services.
• You can continue using existing SOAP integrations that rely on basic authentication while testing or transitioning to OAuth authentication. This helps reduce migration risk and supports phased rollout strategies.
• Ensure that the external token-generation system is available and properly configured before enabling OAuth-based report processing.
• If OAuth token generation fails, workflows using the OAuth-enabled report system may not be able to generate or print reports successfully.
• Existing report definitions, report parameters, and document generation workflows do not require redesign to use this feature.
• Review your organization’s token expiration and rotation policies to avoid authentication interruptions during high-volume reporting operations.
• Validate connectivity between the application, Oracle Analytics Cloud, and the configured external authentication provider in no

---
*Oracle Cloud Readiness · 26C · SCM · Global Trade Management*