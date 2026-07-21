[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# Use Improved Split Order Movement Action

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f46318.htm)

This Optional Feature, when enabled, transitions the split order movement logic to take advantage of the new split order movement logic.  The new split order movement logic allows split planned order movement and order movement on reuse legs.

**Business Benefit:**This Optional Feature serves as a safeguard against unintended regression issues related to the improved split order movement logic.

## ⚙️ Steps to Enable and Configure

If you need to change the Opt In state for this feature:

• Go to the Optional Feature UI - **Configuration and Administration > Property Management > Optional Features**.

Your user must have the DBA.ADMIN user role to use this functionality.

• Select the **Use Improved Split Order Movement Action**feature.
• Run the desired Action for the feature - Opt In or Opt Out

## 💡 Tips and Considerations

**Recommendation:** Enable the feature to validate the updated logic in your environment, and promptly report any issues encountered so they can be addressed before broader adoption.

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*