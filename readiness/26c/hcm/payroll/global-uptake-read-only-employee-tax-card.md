[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Global Uptake: Read Only Employee Tax Card

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f49847.htm)

This feature introduces read-only access to calculation cards for users who require view only visibility to card data. In this release, read-only access is available for the Employee Tax Card for the professional user.

A new aggregate privilege, View Payroll Calculation Cards **(ORA_PAY_VIEW_PAYROLL_CALCULATION_CARDS),** is introduced to support this functionality. This aggregate privilege includes:

• Function privilege: **PAY_VIEW_PAYROLL_CALCULATION_CARDS**
• Data privilege: **PAY_VIEW_PAYROLL_CALCULATION_CARDS_DATA**

The users assigned with the aggregate privilege can view calculation card data but can’t perform any create, update, or delete actions.

In Redwood pages (VBCS), all action buttons, including 'add and date effective actions', are hidden when the user has read-only access. In responsive (ADF) pages, action buttons remain visible, however, users are prevented from performing actions and receive an authorization error upon submission. In both experiences, the Effective Date field remains available, allowing users to view calculation card data as of different dates.

This feature supports read-only access to calculation cards, providing greater control over data access.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

Note these tips and considerations for the feature:

• The **View Payroll Calculation Cards** aggregate privilege is granted to the Payroll Administrator role by default.
• For custom job roles that require read-only access to calculation cards, the new aggregate privilege must be assigned explicitly.

## 📚 Key Resources

Refer to the Administering Payroll for Mexico document located on the Oracle Help Center for additional information.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*