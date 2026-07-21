[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# Suppress Error When No REST RIQ Results Found

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f47439.htm)

This Optional Feature, when enabled, for a REST rate inquiry (RIQ) that returns no results, will be returned with a 200 success status code and empty result as the response. When disabled, the same rate inquiry with no results will return a 500 Internal Server error status code.

**Business Benefit:** This feature improves how the system responds to rate inquiries (RIQ) scenarios where no matching rates are available by treating “no results found” as a valid business outcome rather than an error. When enabled, the system returns a successful response along with an empty result set, clearly indicating that the request was processed correctly but no applicable rates were found. The clear "no results found" information avoids unnecessary troubleshooting.

## ⚙️ Steps to Enable and Configure

If you need to change the Opt In state for this feature:

• Go to the Optional Feature UI - **Configuration and Administration > Property Management > Optional Features**.

Your user must have the DBA.ADMIN user role to use this functionality.

• Select the**Suppress Error When No REST RIQ Results Found**feature.
• Run the desired Action for the feature - Opt In or Opt Out.

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*