[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Recruiting](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/recruiting.md)

# Redwood Experience: Change Posting Locations of Non-Draft Job Requisitions

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/recr-26c/26C-recruiting-wn-f47333.htm)

You can change the Primary Location and Other Locations fields even when requisitions aren't in the Draft state.

Previously, these fields could only be modified when:

• The requisition was in Draft, or
• The requisition was Open - Posted and had job applications

With this update, you can change the value of these fields when the requisition is:

• In the Job Formatting phase
• Open – Posted and with no job applications

**Business benefits:**

• Increased operational flexibility: Recruiters can quickly adjust job locations without needing to revert requisitions to Draft, reducing delays in the hiring process.
• Faster time-to-post optimization: Teams can correct or refine location details even after posting, ensuring job visibility is aligned with hiring needs.
• Reduced administrative overhead: Eliminates the need for requisition rework or recreation when location updates are required early in the posting lifecycle.
• Improved user control: The new permission model allows organizations to enable flexibility while maintaining control over who can make impactful changes.

## ⚙️ Steps to Enable and Configure

To use Redwood experience, you need to enable the Recruiting Redwood pages profile options. For details, see Set profile options for Redwood pages.

For details on enabling and customizing Redwood for HCM, see How do I adopt Redwood for HCM? and Extending Redwood Applications for HCM and SCM Using Visual Builder Studio

For privileges, see the **Access Requirements** section.

## 💡 Tips and Considerations

• Changing the Primary Location won’t automatically update related or dependent elements (such as candidate selection process).
• Inconsistencies between location and other requisition data may occur if changes aren’t managed carefully.
• It’s recommended that organizations define clear internal guidelines before rolling out this feature widely.

## 🔐 Access Requirements

Users need these privileges:

• New privilege: Update Posting Locations of Job Requisitions Which Can Be Redrafted (IRC_UPDATE_POSTING_LOCATIONS_OF_JOB_REQUISITION_WHICH_CAN_BE_REDRAFTED_PRIV)

• Existing privilege: Update Job Requisition (ORA_IRC_UPDATE_JOB_REQUISITION)

---
*Oracle Cloud Readiness · 26C · HCM · Recruiting*