[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Domestic Violence Leave and Payment

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f49283.htm)

Use Domestic Violence leave to record and pay eligible absences for employees who need time away from work to address urgent matters related to domestic violence.

Improve compliance with Ireland's family leave laws by providing paid domestic violence leave from the first day of absence. Streamline payroll processing with integrated statutory deductions and reporting.

## ⚙️ Steps to Enable and Configure

1. Set up earnings elements.

  •    Do not select Allow multiple entries in the same period.

  •    Ensure earnings elements used in rate definitions have higher priority, meaning a lower number, than the absence elements.

  2. Set up rate definitions and balance feeds.

  •    Create element-category rate definitions for each earnings element.

  •    Add them as rate contributors to Absence Normal Daily Rate.

  •    Set periodicity to Workday and use Periodic Work Schedule Rate Annualized where specified.

  •    For Absence Average Earnings Rate, add balance feeds to Pay for Absence Average Earnings.

  3. Create absence elements and eligibility.

  •    Create absence elements with Absences as primary classification and Domestic Violence as secondary classification.

  •    Use Days, Standard Rate Annualized, and Qualification Absences in the Absence Plan Details section.

  •    Select the placeholder rate definition created earlier and associate the statutory domestic violence absence plan.

  •    Create eligibility for all generated elements.

  4. Create the domestic violence absence plan.

  •    Use Ireland as the Legislation, Qualification as the Plan Type, Calendar Days for UOM, IE Statutory Domestic Violence for the LDG.

  •    Select Transfer absence payment information for payroll processing, select the element created earlier.

  5. Create the absence type.

  •    Use Ireland as the Legislation, Generic absence as the Pattern, Calendar days for UOM, IE Domestic Violence Leave for the LDG, and Active Status.

  •    Add the absence plan with status Active and priority 1.

  •    Enable required display features including Qualified Entitlements for employees, managers, and administrators.

  •    Run Evaluate Absences if changes affect future-dated absences.

For more information on set up and configurations, see How do I set up statutory absences for Ireland?

## 💡 Tips and Considerations

• Domestic Violence leave is paid from day one of absence.
• Entitlement is tracked over a 12-month rolling period, and previously paid days reduce the remaining payable entitlement.
• Use the Daily Normal Pay Override field when a manual override is required for normal daily pay.
• Domestic Violence leave payments are subject to PAYE, PRSI, and USC and should be included in payroll submission reporting.
• Each Domestic Violence absence period should be reviewed with its related absence case setup.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*