[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Risk Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/risk-management.md)

# Changes Are Made to Business Objects

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/risk26c/26C-risk-wn-f47370.htm)

This release includes changes to five business objects and introduces one new Project Manager object.

**New Business Object Attributes**

The following business objects have been updated with new attributes.

Business Object | New Attributes
Audit - Contract | EligibleForIngestionYn New EligibleForIngestionYn Old LastIngestionDate New LastIngestionDate Old
Audit - Item | Expiration Date Calculation Basis New Expiration Date Calculation Basis Old
Audit - Person Allocated Checklist Tasks | AttachmentTypeTags New AttachmentTypeTags Old DocumentTypeTags New DocumentTypeTags Old DynamicNotesSource New DynamicNotesSource Old DynamicNotesType New DynamicNotesType Old
Audit - Value Set | Hybrid search enabled New Hybrid search enabled Old

**Note:** There is no way to revise an existing control with the new attribute.

**Attribute Name Change**

The **Project Manager** attribute in the Projects business object is returning an incorrect value. You cannot rely on this attribute for correct information and its label was changed to **Project Manager - Unavailable**. A new business object is described in the next section where you can retrieve the correct value.

**New Business Object**

One new business object is now available called **Project Manager****.**This new business object was introduced to support information regarding a project's manager. **Project Manger** is the replacement to support the information that is not available in Projects business object. The new**Project Manager** business object has a direct delivered relationship to Projects object.

## 🎯 Business Benefit

Enhancements to the audit business objects ensure continued alignment with records in *Setup and Maintenance > Manage Audit Policies*, while the introduction of the new Project Manager object delivers more precise and reliable ownership visibility across projects.

## ⚙️ Steps to Enable and Configure

When you use business objects that introduce changes to attributes, you must run the Transaction Data Source Synchronization job. Business objects with changes require that the data synchronization job be run to return the related values. Depending upon the number of business objects you are using across models and controls, the data synchronization job may take a little longer than usual.

---
*Oracle Cloud Readiness · 26C · ERP · Risk Management*