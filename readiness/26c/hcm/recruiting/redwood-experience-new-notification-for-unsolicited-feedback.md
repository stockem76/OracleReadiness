[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Recruiting](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/recruiting.md)

# Redwood Experience: New Notification for Unsolicited Feedback

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/recr-26c/26C-recruiting-wn-f44404.htm)

A new notification is available in Alerts Composer to inform the recruiter that unsolicited feedback was provided:

• Unsolicited Feedback Completed (IRC_Feedbk_Completed_Unsolicited)

**Business benefit:** Gives more flexibility to route these notifications to the most appropriate recipients instead of always sending them to the recruiters. It also allows defining notification content specifically for unsolicited feedback.

## ⚙️ Steps to Enable and Configure

The tokens available to be used as recipients for the new unsolicited feedback notification (IRC_Feedbk_Completed_Unsolicited) are:

• RequisitionRecruiterUserName (recipient token used in the seeded content of the notification)
• RequisitionHiringManagerUserName
• FeedbackRequestorUserName

Since we're in the context of an unsolicited notification, the requestor is considered to be the respondent of the feedback request.

## 📚 Key Resources

• Redwood Experience: Provide Feedback

---
*Oracle Cloud Readiness · 26C · HCM · Recruiting*