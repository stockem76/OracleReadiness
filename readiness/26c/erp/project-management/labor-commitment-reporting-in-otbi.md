[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Project Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/project-management.md)

# Labor Commitment Reporting in OTBI

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/ppm26c/26C-ppm-wn-f49352.htm)

Leverage Oracle Transactional Business Intelligence, or OTBI, to report on labor commitment information for project planning and control. Labor commitment reporting helps you analyze future labor commitments and related cost distributions so you can validate project spend, review commitment liquidation, and manage labor-related project costs more efficiently.

With this update, additional labor commitment and labor distribution attributes are available in existing OTBI subject areas. These attributes help project managers, grants administrators, and financial analysts evaluate labor commitments alongside actual labor cost information and improve visibility into labor-related project obligations.

**Labor Distribution Cost Analysis Reporting Enhancements**

The **Projects - Labor Distribution Cost Analysis Real Time** subject area includes additional labor cost distribution details. The following attribute is added to the **Labor Cost Distribution Details** folder:

• Liquidation Project Payroll Cost

This attribute supports reporting on labor commitment-related cost distributions and helps users identify whether distributed costs are associated with commitment liquidation activity.

**Project Commitment Reporting Enhancements**

The **Project Costing Commitments Real Time** subject area is enhanced with additional person and labor-related attributes that align more closely with attributes available for actual project costs. The added attributes include:

**Employee Folder**

• Employee Name
• Person ID
• Person Number
• Employee Email Address
• Employee Business Unit

**Job Folder**

• Job Code
• Job Name
• Job Active Status

**Commitment Folder**

• Assignment Name
• Assignment Number
• Assignment Start Date
• Assignment End Date
• Assignment Sequence
• Cost Action ID
• Cost Action Type
• Funds Status
• Job ID
• Payroll ID
• Payroll Name
• Pay Element
• Pay Element ID
• Person Type
• Adjusting Item
• Liquidation Flag

These attributes provide more complete labor commitment reporting and help users analyze commitments by employee, assignment, payroll, job, and pay element.

**Business Benefits**:

• Get clear visibility into labor commitments and related costs.
• Easily track and validate commitment liquidation.
• Quickly trace costs back to original commitment transactions.
• Analyze commitments with detailed employee and payroll information.
• Make better project decisions by comparing commitments with actual costs.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

Consider these points when using the new labor commitment reporting attributes:

• Use the **Liquidation** or **Liquidation Flag** attributes to distinguish commitment liquidation activity in reports.
• Use person, assignment, payroll, job, and pay element attributes to analyze labor commitments at a more detailed level.
• Compare labor commitment information with actual labor cost reporting to improve project spend planning and control.

## 🔐 Access Requirements

Duty roles needed to access the subject areas are:

• Projects - Labor Distribution Cost Analysis Real Time (Subject Area) 
  • Project Labor Distributions Transaction Analysis Duty
• Project - Costing Commitments Real Time (Subject Area) 
  • Only one of the Duty roles below are required: 
    • Project Costing Transaction Analysis Duty
• Grants Management Transaction Analysis Duty

## 📚 Key Resources

• The Projects - Labor Schedule Analysis Real Time and the Projects – Labor Distribution Cost Analysis Real Time subject areas in the Subject Areas for Transactional Business Intelligence in Project Management guide.
• Creating and Administering Analytics and Reports for Project Management guide.
• The Labor Distribution Administrator and Labor Distribution Accountant roles in the Security Reference for Project Management guide.

---
*Oracle Cloud Readiness · 26C · ERP · Project Management*