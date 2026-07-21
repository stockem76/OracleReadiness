[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Recruiting](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/recruiting.md)

# Redwood Experience: More Use Cases for Defaulting and Validation Rules for Create Job Requisition Flow

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/recr-26c/26C-recruiting-wn-f47363.htm)

Here are additional use cases to default the value of fields when creating job requisitions:

• Default the value of the Hiring Manager field with the position's Department Manager.
• Default the value of the job requisition descriptive flexfields (DFF) with the value of the department’s DFFs.
• Display an error message when the value of the location DFFs doesn’t match the value of the Legal Employer field in the requisition .
• Default the value of the Currency and Frequency fields on the job requisition with the Grade Rate Currency and Frequency values.

Additionally, more business rules are available for the fields in the career sites sections of the Posting tab. You can hide or making some fields read-only for specific users based on your business requirements.

**Business benefits:**

• Increased data accuracy and alignment: Defaulting values from Position, Department, Location, and Grade Rate ensures that job requisitions are automatically aligned with core workforce structures, reducing inconsistencies and manual data entry errors.
• Improved efficiency and faster requisition creation: Prepopulating fields such as Hiring Manager, Currency, Frequency, and DFFs streamlines the requisition creation process, enabling users to complete tasks more quickly with less effort.
• Stronger validation and compliance controls: Enhanced validation using the business rules framework helps enforce organizational policies and prevents incorrect or non-compliant data from being submitted.
• Greater flexibility and configuration control: The ability to configure field behavior (hide or make read-only) in the career site sections allows organizations to tailor the experience based on user roles and business needs without requiring custom development..

## ⚙️ Steps to Enable and Configure

To use Redwood experience, you need to enable the Recruiting Redwood pages profile options. For details, see Set profile options for Redwood pages.

For details on enabling and customizing Redwood for HCM, see How do I adopt Redwood for HCM? and Extending Redwood Applications for HCM and SCM Using Visual Builder Studio

---
*Oracle Cloud Readiness · 26C · HCM · Recruiting*