[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# LGPS Stringer Days

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f47420.htm)

With the LGPS Stringer Days which apply during a period of sickness, you can:

• Configure Stringer Days as a vacation-like accrual absence plan and generic absence type,
• Identify the absence type with the UK Stringer Days legislative grouping,
• Enable concurrent entitlement,
• Process Stringer Days payments through payroll during a sickness absence.

A new seeded ORA_HRX_GB_STRINGER_DAYS certificate supports pausing statutory sick pay at the case level and occupational sick pay at the absence entry level while the employee is on Stringer Days leave.

When Stringer Days are paid during reduced sick pay that triggers LGPS Assumed Pensionable Pay, the payroll calculation compares the daily Stringer Days payment with the APP daily rate and feeds the higher amount to CPP1 and CPP2. APP remains unchanged after the Stringer Days period.

This feature helps UK LGPS payroll and absence administrators process annual-leave-like Stringer Days during sickness absence while preserving SSP and OSP entitlement, resuming sickness payments after the Stringer Days period, and calculating pensionable pay correctly.

## ⚙️ Steps to Enable and Configure

1. Create a new LGPS pension element to get the affected formula changes automatically.
• If you don't create a new element, please follow the steps described in document 'Stringer Days Setup: Changes to Support Pension Calculations when Stringer Days are Paid' and do the formula changes manually
2. Absence Plans 
  • As Stringer Days is similar to Vacation, create the absence plan as 'Accrual Plan'.
• Assign the Plan UOM, the Plan Term, Eligibility (if required), Entitlements, and the Entries and Balances.
• The absence plan should be created to allow concurrent entitlement.
• If you want to transfer vacation days to Stringer Days, use the Entries and Balances tab on the absence plan page of your Vacation plan to enable 'Balance transfer across plans' accrual plan adjustments.

     This should allow HR specialists to make adjustments to plan balances on the Manage Absence Records and Entitlements page.
• To make adjustments, HR specialists can select an option on the Enrollments and Adjustments menu of the Plan Participation section.
3. Absence Types 
  • The Stringer Days absence type should be created as a Generic Absence, with Legislative Grouping Code set to UK Stringer Days.
• In the absence type for Stringer Days, open the Display features and select 'Enable Concurrency'.
• In the absence type for Statutory Sickness, open the Action items and add the certificate 'Stringer Days'.

**Note:**

• For Stringer Days, there is a new seeded ORA_HRX_GB_STRINGER_DAYS certificate.
• You will need to create ORA_HRX_GB_STRINGER_DAYS certificate at Absence Case level for the SSP Plan and ORA_HRX_GB_STRINGER_DAYS certificate at absence entry level for the Occupational Sickness Plan, if you want to stop all sickness payments during Stringer Days leave.

4. Absence Entries

• When entering the Stringer Days absence and you want to make adjustments from the vacation plan, HR specialists should be able to select an option on the Enrollments and Adjustment  menu of the Plan Participation section. 
  • Under Plan Participation, select the vacation plan and then click the Enrollments and Adjustments dropdown.
• An option for transfer of balance will be available.
• Click and add the Effective Date, the Plan to which the balance has to be transferred and the Number of Days to be transferred.
• Then run the accrual process, the balance of the Stringer Days plan will be updated.

5. Attach the absence records for Sickness and as well for Stringer Days and then go to Absence Case for the sickness absence and add the certificate to pause the statutory sick pay, or absence entry level to pause the occupational sick pay.

**Note:**

• When adding the certificate to the person, ensure that the dates correspond to the Stringer Days absence, other wise calculations will be inaccurate.
• Where there are multiple assignments, the same number of Stringer Days will be expected for each assignment.

6. Ensure that the Pension Element's Balance 'Eligible Compensation' is fed with the absence's Entitlement Result, that is both sickness and stringer days entitlement results

## 💡 Tips and Considerations

• Certificate dates must correspond to the Stringer Days absence dates to avoid inaccurate calculations.
• For employees with multiple assignments, use the same number of Stringer Days for each assignment.
• The number of Stringer Days paid should not exceed the employee's remaining normal vacation days.
• APP isn't recalculated after the Stringer Days period. It remains the same for the rest of the absence period.

## 🔐 Access Requirements

Payroll and absence administrators need access to configure absence elements, absence plans, absence types, certificates, absence cases, absence entries, plan balance transfers, and payroll balance feeds.

## 📚 Key Resources

For more details, refer to: https://docs.oracle.com/en/cloud/saas/human-resources/fapsk/stringer-days-setup-and-management.html

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*