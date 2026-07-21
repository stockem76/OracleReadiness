[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Carer's Leave Entitlement

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f49279.htm)

Use Carer's leave to record extended unpaid leave for employees who need to provide full-time care and attention. The absence setup enforces the entitlement conditions defined for Ireland, including maximum duration, minimum duration, and the minimum gap required between periods of leave.

Improve legislative compliance by accurately tracking and enforcing Carer's leave entitlements under Ireland's family leave requirements. Reduce errors by providing clear messaging when leave requests exceed allowed limits. Simplify management of unpaid family leave with enforced duration and gap rules.

## ⚙️ Steps to Enable and Configure

1.   Create the Carer’s Leave validation formula:

  •    Go to the fast formula setup area and create a Global Absence Entry Validation formula ORA_HRX_IE_CARE_VALIDATION based on the delivered seeded formula IE Carers Absence Validation Included.

  •    Use the formula to validate the statutory rules for Ireland Carer’s Leave, including maximum duration of 104 weeks, minimum duration of 13 weeks, minimum one year of service, and minimum six-week gap between Carer’s Leave blocks.

  2.   Create the Carer's leave absence plan with 'Ireland' as the Legislation and 'Qualification' as the Plan Type.

  3.   Create the Carer's leave absence type with 'Ireland' as the Legislation and 'Generic absence' as the Pattern:

  •    Set the UOM to 'Calendar days' or 'Days', select the Validation formula created earlier, and set the Status to 'Active'.

  •    Do not select multiple assignment rule check boxes, because the setup supports absences only at person level.

  4.   Associate the absence type with the absence plan and configure display options for various fields. Ensure that the Status is 'Active' and the Priority is 1.

For more information on set up and configurations, see How do I set up statutory absences for Ireland?

## 💡 Tips and Considerations

• Carer's leave is unpaid.
• The entitlement configuration should enforce the maximum and minimum duration limits and the minimum gap between periods of leave.
• Use the Notice Received legislative field to record whether notice has been received for the leave period.
• Users receive a message when they attempt to record a Carer's leave absence that exceeds the maximum allowed duration.
• Validate the absence type, absence plan, and entitlement rules together to make sure the leave behaves correctly at entry time.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*