[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Human Resources](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/human-resources.md)

# Redwood Enabled by Default for Employment Pages in Update 27A

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hure-26c/26C-hr-wn-f50060.htm)

Enhance the user experience by letting users directly access the following Redwood-enabled Employment pages where the Redwood profile option is turned on by default in 27A.

This table shows the Redwood pages where the profile options will be enabled by default from update **27A**onward:

Redwood Page | Profile Option Code | First Release of Redwood Page
Resign From Employment | ORA_PER_EMPL_RESIGNATION_REDWOOD_ENABLED | 24C
Mass Assignment Change | ORA_PER_EMPL_MASS_ASG_UPDATE_REDWOOD_ENABLED * | 26D
Terminate Employment | ORA_PER_EMPL_TERMINATE_REDWOOD_ENABLED | 24C

* This Redwood page will be available from release 26D onward.

Users can quickly and easily access the Employment Redwood pages by using the quick action for the respective page.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

If you want to, you can disable the profile option (set to No) for the Redwood pages where it's enabled. To do so, follow these steps:

1. Navigate to the Setup and Maintenance work area.
2. Search for and click the **Manage Administrator Profile Values** task.
3. Search for the profile option code that you want to disable and select the profile option in the search results.
4. In the Profile Values area, enter **No**in the **Profile Value** field.
5. Click **Save and Close**.
6. Click **Done**.

## 📚 Key Resources

For more information, refer to this document on My Oracle Support: HCM Redwood Pages with Profile Options (Doc ID 2922407.1)

---
*Oracle Cloud Readiness · 26C · HCM · Human Resources*