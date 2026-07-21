[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# SMD Sync With Order On SSU Count Increase

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f47438.htm)

This Optional Feature, when enabled, and the shipment actual (SMD) is received, the unplanned order movement count is synced with the planned order movement in case there is an increase in the ship unit count.

**Business Benefit:** This feature helps you to maintain accurate and consistent data between shipments and orders by:

• Reducing manual reconciliation effort when shipment counts change
• Preventing data mismatches that can impact billing, planning, or reporting

## ⚙️ Steps to Enable and Configure

If you need to change the Opt In state for this feature:

• Go to the Optional Feature UI - **Configuration and Administration > Property Management > Optional Features**.

Your user must have the DBA.ADMIN user role to use this functionality.

• Select the**SMD Sync With Order On SSU Count Increase**feature.
• Run the desired Action for the feature - Opt In or Opt Out.

## 💡 Tips and Considerations

This optional feature replaces the property glog.business.shipmentactual.syncWithOrderOnCountIncrease.

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*