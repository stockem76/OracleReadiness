[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Redwood Experience for Calculation Cards Enabled by Default for Professional Users

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f49491.htm)

In this release, Redwood profile option is now enabled by default for the following calculation cards:

Calculation Card | Profile Option
Tax Credit Information for professional users | ORA_HRX_CA_ADMIN_TAXCREDITINFORMATION_VBCS_ENABLED
Reporting Information | ORA_HRX_CA_REPORTINGINFORMATION_VBCS_ENABLED

The pages are not displayed in Redwood by default. The following core profile options must also be set to **Yes** at the site level for both pages to display in Redwood:

• ORA_PAY_CALC_ENTRIES_LANDING_REDWOOD_ENABLED
• ORA_HCM_VBCS_PWA_ENABLED.

To enable the profile options, navigate to **Setup and Maintenance** and select the **Tasks** menu. Click Search, and search for **Manage Administrator Profile Values**. Search for each profile option code and set the value to **Yes** at the site level.

The Redwood Experience provides a more modern, intuitive interface.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• From Update 27A onward, we will only support the Redwood versions of these calculation cards.
• The Redwood calculation cards are accessible from the following navigation paths:
• Tax Credit Information (Admin): 
• My Client Groups > Payroll > Earnings and Deductions
• My Client Groups > Payroll > Calculation Entries
• Reporting Information: My Client Groups > Payroll > Calculation Entries

## 📚 Key Resources

Refer to these documents located on the Canada Information Center (KA144) for additional information.

**Implementing Payroll for Canada**

• CA – Payroll tab > Product Documentation > Payroll Guides > Implementing Payroll for Canada

**Administering Payroll for Canada**

• CA – Payroll tab > Product Documentation > Payroll Guides > Administering Payroll for Canada

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*