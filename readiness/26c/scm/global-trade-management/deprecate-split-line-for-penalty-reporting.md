[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Global Trade Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/global-trade-management.md)

# Deprecate Split Line For Penalty Reporting

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/gtm26c/26C-gtm-wn-f49604.htm)

This optional feature deprecates the existing **Split Line for Penalty Reporting** action and replaces it with enhanced functionality provided through the new **Apply Tariff Unstacking Rules** action.

With the increasing number of penalty tariffs, there may be situations where multiple overlapping penalty tariffs apply to a product being imported. To prevent multiple penalty tariffs from being charged simultaneously, governments may enforce rules that apply only the highest tariff or a specific combination of tariffs. GTM has been enhanced to better support these regulatory requirements. As part of this enhancement, the new **Apply Tariff Unstacking Rules** action can split lines based on applicable regulations and GTM configuration.

When this optional feature is set to **Opt In**:

• The penalty classification code value on the **Tariff Rate** record is not populated.
• The **Split Allowed** flag on the **Trade Program** is not populated.
• The **Split Line for Penalty Reporting** web action and agent action will no longer execute and will instead return the error:
*“The action is deprecated.”*

**Note:** It is recommended that you discontinue use of the **Split Line for Penalty Reporting** action and use the new **Apply Tariff Unstacking Rules** action instead.

**Business Benefit:** This feature helps organizations comply with evolving tariff regulations by providing improved consistency in penalty reporting outcomes and reduces reporting complexity and potential user confusion.

## ⚙️ Steps to Enable and Configure

If you need to change the Opt In state for this feature:

• Go to the Optional Feature UI - **Configuration and Administration > Property Management > Optional Features**.

Your user must have the DBA.ADMIN user role to use this functionality.

• Select the **Deprecate Split Line For Penalty Reporting**feature.
• Run the desired Action for the feature - Opt In or Opt Out

## 📚 Key Resources

For more information on enhancements to penalty codes/penalty exemption codes and the new Apply Tariff Unstacking Rules action, refer to the "Enhanced Support for Penalty Codes and Penalty Exemptions Codes" topic in this document.

For more information on splitting penalty lines, refer to the "Enhancements to Tracking and Reporting of Penalty Content" topic in the 26B What's New document.

---
*Oracle Cloud Readiness · 26C · SCM · Global Trade Management*