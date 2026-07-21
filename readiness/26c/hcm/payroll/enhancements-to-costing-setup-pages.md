[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Enhancements to Costing Setup Pages

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f50582.htm)

The Redwood Costing Setup pages now retain key page context to streamline navigation and reduce repetitive data entry.

When you perform **Update** or **End Date** actions, the application retains the selected **Effective As-of Date** if it's valid for the selected costing record. If the selected **Effective As-of Date** falls outside the selected costing record's effective date range, the application defaults to the record's **Effective Start Date** during an **Update** operation and to the **Effective End Date** during an **End Date** operation.

The application also preserves the selected **Legislative Data Group** and **Effective As-of Date** when you switch between costing levels, allowing you to continue working without having to reselect these values. If you have a **Default Saved Search**, it continues to take precedence over retained filter values.

This enhancement reduces repetitive data entry and provides a more consistent experience across costing levels.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*