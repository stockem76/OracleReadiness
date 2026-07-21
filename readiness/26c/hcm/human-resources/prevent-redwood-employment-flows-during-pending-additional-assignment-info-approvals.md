[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Human Resources](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/human-resources.md)

# Prevent Redwood Employment Flows During Pending Additional Assignment Info Approvals

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hure-26c/26C-hr-wn-f49407.htm)

When an Additional Assignment Info transaction is pending approval then the Redwood flows now follow the same approval-based blocking behavior as the existing Responsive flows. This provides consistent transaction conflict handling across both experiences.

This enhancement applies to the affected Redwood employment flows out of the box. No profile option or additional setup is required.

• Change worker type
• Add assignment
• Local and global transfer

Employment update processes such as Change Assignment, Promote, and Change Location already show the pending approval message in the Additional Assignment Info section and continue to use that existing behavior.

Transaction is locked if it's pending approval

This enhancement improves consistency and data integrity across Redwood and Responsive employment flows. It reduces the chance of conflicting in-flight assignment updates, helps avoid approval completion failures, and gives users clearer guidance when another assignment transaction is already pending.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 📚 Key Resources

For more information, refer to this resource on the Oracle Help Center

• Employment Processes in the Using Global Human Resources guide

---
*Oracle Cloud Readiness · 26C · HCM · Human Resources*