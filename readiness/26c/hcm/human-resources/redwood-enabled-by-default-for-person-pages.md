[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Human Resources](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/human-resources.md)

# Redwood Enabled by Default for Person Pages

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hure-26c/26C-hr-wn-f47440.htm)

Effective from release 26C, the Redwoodperson pages will be enabled by default. These are the impacted pages:

• Personal Details
• Contact Info
• Identification Info
• Family and Emergency Contacts
• Additional Person Info
• Person Identifiers for External Applications

The corresponding responsive pages will no longer be available by default. However, you can still access them by manually setting the relevant profile option to **No**. You can see the list of profile options for all these pages in the **Steps to Enable and Configure** section of this What's New.

By using these new pages, you can take advantage of the cohesiveness through the application.

## ⚙️ Steps to Enable and Configure

If you want to, you can disable the profile options for the Redwood pages where they're enabled. You can do so by entering **No**in the **Profile Value** field. Follow these steps: How do I enable a profile option?

This table lists the profile option codes for Redwood Person pages.

Redwood Page | Profile Option Code
Personal Details | ORA_PER_PERSONAL_INFORMATION_REDWOOD_ENABLED
Contact Info | ORA_PER_PERSONAL_INFORMATION_REDWOOD_ENABLED
Identification Info | ORA_PER_PERSONAL_INFORMATION_REDWOOD_ENABLED
Family and Emergency Contacts | ORA_PER_PERSONAL_INFORMATION_REDWOOD_ENABLED
Additional Person Info | ORA_PER_ADDITIONAL_PERSONAL_INFO_REDWOOD_ENABLED
Person Identifiers for External Applications | ORA_PER_PERSON_IDENTIFIERS_FOR_EXT_APP_REDWOOD_ENABLED

## 🔐 Access Requirements

The roles that had access to the responsive pages will have access to the corresponding Redwood page as well.

If you're using custom roles, take note of this change for managing addresses in Redwood pages, that was added in 24D: Privilege Changes for Managing Addresses in Redwood Pages

## 📚 Key Resources

For more information on the profile options, refer to this document on My Oracle Support: HCM Redwood Pages with Profile Options (Doc ID 2922407.1)

The list below provides details on the features delivered in the initial release of the Redwood pages, along with significant enhancements introduced in subsequent updates.

Personal Details

• 24A: Redwood Experience for Personal Info Pages
• 24C: Control the Display of Add and Edit Icons for National Identifiers and Biographical Info on the Redwood Personal Details Page
• 25A: National Identifiers are Masked on Redwood Pages
• 25A: Change Person Photo Incorporated into Redwood Personal Details Page
• 25B: New Page Properties to Control the Add Action on Redwood Personal Info Pages
• 25B: Religion, Ethnicity, Do You Have a Disability, and Disability Reason Fields Are Masked on Read-Only Redwood Pages
• 26A: Name Section of Redwood Personal Details Page is Integrated with Document Records
• 26B: Expanded Document Records Integration for Redwood Personal Details and Identification Info Pages

Contact Info

• 24A: Redwood Experience for Personal Info Pages
• 25B: New Profile Option Added and Blind Query Removed for Redwood Address LOVs
• 25B: New Page Properties to Control the Add Action on Redwood Personal Info Pages
• 25D: New Profile Option for Enabling Blind Query in Redwood Address LOVs

Identification Info

• 24A: Redwood Experience for Personal Info Pages
• 25B: New Page Properties to Control the Add Action on Redwood Personal Info Pages
• 26B: Expanded Document Records Integration for Redwood Personal Details and Identification Info Pages

Family and Emergency Contacts

• 24A: Redwood Experience for Personal Info Pages
• 25B: New Page Properties to Control the Add Action on Redwood Personal Info Pages
• 25D: Access Redwood Additional Person Info for Contacts

Additional Person Info

• 24A: Redwood Experience for Additional Person Info
• 24B: Benefit from Redwood Additional Person Information Approval Support
• 25B: New Page Properties to Control the Add Action on Redwood Personal Info Pages
• 25B: Prior Records are Displayed on the Redwood Additional Person Info Page
• 26A: Additional Person Info Multi-row Records Displayed in Table Format

Person Identifiers for External Applications

• 23B: Redwood Experience for Person Identifiers for External Applications
• 25B: New Page Properties to Control the Add Action on Redwood Personal Info Pages

---
*Oracle Cloud Readiness · 26C · HCM · Human Resources*