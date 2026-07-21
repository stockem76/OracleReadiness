[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Compensation](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/compensation.md)

# Total Compensation Statement: Redwood Experience for Statement Definitions

`🔧 Optional Uptake` · `⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/comp-26c/26C-compensation-wn-f49867.htm)

Check out the new Statement Definitions page re-created with the Redwood tool set Visual Builder Studio (VBS). You can enable the page along with the Redwood experience.

Statement Definitions

Statement Definition

Periods

With this re-created Redwood page, you continue your journey into Oracle Redwood solutions.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Compensation Management*

Enable these profile options to use the new Welcome Message page. To revert to the non-Redwood page, set the site-level profile value to No for this profile option. To configure a profile option, complete these steps in the Setup and Maintenance work area:

1. Search for and click the **Manage Administrator Profile Values**task.
2. Search for and select the profile option.
3. Set the Level to **Site**.
4. In the Profile Value field, select a value.

Profile Option Code | Profile Option Description | Value
ORA_HCM_VBCS_PWA_ENABLED | Enable VBCS Progressive Web Application User Interface | Y
ORA_CMS_TOTAL_COMPENSATION_STATEMENTS_REDWOOD_ENABLED | Redwood Total Compensation Statements Enabled | Yes
ORA_CMS_TOTAL_COMPENSATION_STMT_SETUP_REDWOOD_ENABLED | Redwood Total Compensation Setup Enabled (new) | No

The default value for this new profile is No. Only when all 3 profiles are enabled, will you see the redwood version of the Statement Definition setup page.

## 📚 Key Resources

For a listing of all profile options for the recreated pages across applications, see the following document in My Oracle Support: HCM Redwood Pages with Profile Options - Document ID 2922407.1

---
*Oracle Cloud Readiness · 26C · HCM · Compensation*