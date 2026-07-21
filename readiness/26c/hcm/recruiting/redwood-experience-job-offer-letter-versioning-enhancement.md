[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Recruiting](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/recruiting.md)

# Redwood Experience: Job Offer Letter Versioning Enhancement

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/recr-26c/26C-recruiting-wn-f47371.htm)

This enhancement adds version control for job offer letters, ensuring consistency between the version presented to candidates and the one retained for record-keeping.

Previously, if an offer letter template was modified after an offer was extended, the system could display or store a newer version instead of the original. This created potential compliance issues. With this update, the system preserves and stores the exact version of the offer letter that was in place at the time the offer was extended.

Here's how it works.

• The offer letter version is locked when the offer is extended. The same version is: 
• Viewed by the candidate
• Used during signing
• Stored in the Document of Record (DOR)

• If the offer letter template is updated before the offer is extended, the latest version is used for both preview and extension.

• When an offer is redrafted, the version is: 
• Cleared
• Reset to use the latest available template version
• For offers in inactive states (such as Processed, Withdrawn by Candidate, Abandoned, Assignment Terminated), offer preview remains available. The system determines the appropriate version based on the offer’s extended date.

**Business benefits:**

• Improved compliance and audit readiness: Ensures that the exact offer letter viewed and accepted by the candidate is the same version stored in official records.
• Enhanced data integrity: Eliminates discrepancies caused by template updates after offer extension, ensuring accurate documentation.
• Better candidate experience: Candidates review and sign a consistent offer letter without unexpected changes.
• Increased administrative control: Configuration setting allows organizations to enable versioning based on their compliance and business needs.

## ⚙️ Steps to Enable and Configure

**Step 1: Select the Enable versioning of job offer option**

Go to Setup and Maintenance > Recruiting and Candidate Experience > Recruiting and Candidate Experience Management > Enterprise Recruiting and Candidate Experience Information > Offer.

**Step 2: Run the Manage Recruiting Job Offer Letters scheduled process**

Go to Navigator > Tools > Scheduled Processes > Schedule New Process.

---
*Oracle Cloud Readiness · 26C · HCM · Recruiting*