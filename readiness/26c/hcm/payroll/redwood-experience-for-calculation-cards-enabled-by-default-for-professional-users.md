[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Redwood Experience for Calculation Cards Enabled by Default for Professional Users

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f49838.htm)

The Redwood profile option is now enabled by default for the Employee Tax Card for the professional user. The **ORA_HRX_MX_ADMIN_EMPLOYEETAXCARD_VBCS_ENABLED** profile option is now set to **Yes**.

The pages aren't displayed in Redwood by default. The following core profile options need to be set to **Yes** at the site level for the Employee Tax Card page to display in Redwood:

• ORA_PAY_CALC_ENTRIES_LANDING_REDWOOD_ENABLED
• ORA_HCM_VBCS_PWA_ENABLED.

To enable these profile options, navigate to **Setup and Maintenance** and select the **Tasks** menu. Click Search, and search for **Manage Administrator Profile Values**. Search for each profile option code and set the value to **Yes** at the site level.

The Redwood Experience provides a more modern, intuitive interface.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

From Update 27A onward, we will only support the Redwood version of the Employee Tax Card.

The Redwood version of the Employee Tax Card is accessible from the following navigation paths:

• My Client Groups > Payroll > Earnings and Deductions
• My Client Groups > Payroll > Calculation Entries

## 📚 Key Resources

Refer to the Administering Payroll for Mexico document located on the Oracle Help Center for additional information.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*