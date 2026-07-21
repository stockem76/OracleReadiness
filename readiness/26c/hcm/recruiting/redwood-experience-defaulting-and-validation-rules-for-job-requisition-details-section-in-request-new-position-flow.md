[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Recruiting](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/recruiting.md)

# Redwood Experience: Defaulting and Validation Rules For Job Requisition Details Section in Request New Position Flow

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/recr-26c/26C-recruiting-wn-f47334.htm)

You can personalize the job requisition details section in Redwood Request New Position flow using new defaulting and validation rules in Visual Builder Studio.

These use cases are supported:

• Default the value of the Business Justification field to New Position.
• Default the value of the Business Justification field when creating a new position.
• Validate the value of the Business Justification field when creating a job requisition using a position.
• Default the value of the Recruiting Type field based on a job attribute.
• Default the value of the Organization field based on the position's department.
• Default the value of the Primary Location field based on the position's work location.
• Default the value of the Hiring Manager field with the signed in user.
• Validation rules on the fields in the requisition Details section based on the job name.

Additionally, we have exposed more fields for **Opening type** field in the requisition details section of Redwood Position flows, Currently, there's only 1 field **Opening type** exposed in Visual Builder Studio for the Requisition Details section in the Position flows. To bring parity with the Redwood create requisition and edit requisition pages, we're exposing 3 fields to individually default unlimited opening, number of hire, and hide or show whole Opening type field.

You can now see these fields in Visual Builder Studio for Requisition Details section in Position flows:

• Opening Type
• Number of Openings
• Unlimited Openings Flag

**Business benefits:**

• Improved data accuracy and consistency: Automatic defaulting of key fields (such as Business Justification, Recruiting Type, Organization, Location) ensures that the requisition Details section is populated with consistent and reliable data, while requesting for a new position.
• Faster position request process: Prepopulated fields and smart defaults minimize manual input, enabling users to complete the Request a New Position flow more efficiently and with fewer steps.
• Stronger data validation and compliance: Built-in validation ensures that required information is captured based on job type, helping organizations maintain compliance with internal policies and avoid incomplete or incorrect requisitions.
• Enhanced user experience: Context-aware defaults (Hiring Manager as signed-in user, conditional required fields) simplify the process and guide users, making the system more intuitive and reducing confusion during position creation.

## ⚙️ Steps to Enable and Configure

To use Redwood experience, you need to enable the Recruiting Redwood pages profile options. For details, see Set profile options for Redwood pages.

For details on enabling and customizing Redwood for HCM, see How do I adopt Redwood for HCM? and Extending Redwood Applications for HCM and SCM Using Visual Builder Studio

---
*Oracle Cloud Readiness · 26C · HCM · Recruiting*