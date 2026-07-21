[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# Honor Update Flag For REST RefNum Updates

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f43369.htm)

This Optional Feature, when enabled, allows updates to the reference numbers via REST based on the Updates Allowed configuration of the reference number qualifier when adding a Reference Number using the REST API.  The persistence behavior is determined by the Updates Allowed configuration for the related Reference Number Qualifier.

Previously, when updating a Reference Number using the REST services, a new Reference Number was created without considering the configuration of the Update Flag on the related Reference Number Qualifier.

The Update Flags available on the Reference Number Qualifier are:

• One, Update: existing value is replaced with the value from the inbound message.
• One, Do not Update: existing value is retained and the data in the inbound message are ignored.
• Many: values in the inbound message are added as new remarks/references. However, if a remark sequence number is also present in the inbound message, then any existing value for the combination of remark qualifier and sequence number will be replaced.

**Business Benefit:** This feature provides equivalence between the behavior of the XML APIs and the REST Services for how the Update Flag on the Reference Number Qualifier are handled.

## ⚙️ Steps to Enable and Configure

If you need to change the Opt In state for this feature:

• Go to the Optional Feature UI - **Configuration and Administration > Property Management > Optional Features**.

Your user must have the DBA.ADMIN user role to use this functionality.

• Select the**Honor Update Flag For REST RefNum Updates**feature.
• Run the desired Action for the feature - Opt In or Opt Out.

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*