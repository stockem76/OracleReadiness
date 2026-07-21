[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Redwood Enabled by Default for UK Payroll

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f49820.htm)

Enhance the user experience by letting users directly access Pension Enrollment and New Starter Declaration Redwood-enabled HCM pages where the Redwood profile option is turned on by default in 26C.

This table shows the Redwood pages where the profile option will be enabled by default from update 26C onward:

Redwood Profile Options

Redwood Page | Profile Option Code | First Release of Redwood Page
Pension Enrollment | ORA_HRX_GB_VBCS_ESS_BP | 24A
New Starter Declaration | ORA_HRX_GB_VBCS_ESS_NSD | 24A

Users can quickly and easily access the payroll related Redwood pages through Employee Self-Service.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

If you want to, you can disable the profile option (set to No) for the Redwood pages where it's enabled. To do so, follow these steps:

1. Navigate to the Setup and Maintenance work area.
2. Search for and click the **Manage Administrator Profile Values** task.
3. Search for the profile option code that you want to disable and select the profile option in the search results.
4. In the Profile Values area, enter **No**in the **Profile Value** field.
5. Click **Save and Close**.
6. Click **Done**.

## 📚 Key Resources

For more information, refer to this document on My Oracle Support: HCM Redwood Pages with Profile Options (Doc ID 2922407.1)

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*