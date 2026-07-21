[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Redwood: Time-Based Autosave in Redwood Performance Documents and All-in-One Evaluations

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f47319.htm)

You can now leverage the time-based autosave for performance documents. Comments and questionnaire responses entered during evaluation tasks are autosaved in Redwood performance documents and in All-in-One Evaluations. This is because autosave is only needed for comments and questionnaires as other changes to ratings are saved as the user navigates around the performance document.

**Business benefit:** This feature enables you to preserve in-progress content and provides a more reliable evaluation experience.

## ⚙️ Steps to Enable and Configure

You need to configure the profile options for Redwood performance documents as indicated in the following table.

Profile Option Code | Description | Value
ORA_HCM_VBCS_PWA_ENABLED | Enable VBCS Progressive Web Application User Interface | Y
ORA_HRA_PERFORMANCE_DOCUMENTS_AND_GOALS_ REDWOOD_ENABLED | Enable performance documents and employee performance and development goals to display in Redwood. | Yes

Configure the following profile option to control the autosave interval:

Profile Option Code | Description | Value
HRA_PERF_AUTOSAVE_ INTERVAL | Controls the time in minutes used to initiate autosave for the open item. | Enter the time in minutes

For more information about setting profile option values, see How do I enable a profile option?

1.    Sign in to the application.

  2.    Open VB Studio Express Mode on the performance document page.

  3.    Under the Common Properties category, set the page property that controls the time-based autosave counter on the performance document page.

  4.    Set the autosave interval using the existing profile option HRA_PERF_AUTOSAVE_INTERVAL

Page Property | Description
Control Time-Based Autosave Counter on the Performance Document Page | This property controls the number of times the autosave counter can be initiated on the performance document page. The default value is 0 and can be set to a maximum of 15.
Control Time-Based Autosave Counter for Comments and Questionnaire Responses in All-in-One Evaluations | This property controls the number of times the autosave counter can be initiated on the performance document page. The default value is 0 and can be set to a maximum of 15.

## 💡 Tips and Considerations

• Time-based autosave applies to evaluation tasks on the performance document page.
• The timestamp appears only for worker self-evaluation, manager evaluation, and participant feedback tasks.
• The timestamp uses the date format defined in the user’s preferences.
• Autosave is triggered only up to the maximum number of times configured in the page property. Content entered after the final autosave and before the next manual or system save isn’t preserved if the session ends unexpectedly

## 📚 Key Resources

• For a listing of all profile options for the recreated pages across HCM, see the following document in My Oracle Support: HCM Redwood Pages with Profile Options – MOS Document 2922407.1
• For more information on extending Redwood pages in HCM, see: Extending Redwood Applications for HCM and SCM Using Visual Builder Studio.

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*