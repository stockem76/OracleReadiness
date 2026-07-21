[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Absence Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/absence-management.md)

# Display Unpaid Break when Absence is Entered on the Timecard

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/amg-26c/26C-absence-mgmt-wn-f49551.htm)

Previously, we introduced a feature in 26B to display unpaid break on the absence Redwood pages when the break is automatically deducted from the absence duration. This wasn't supported for absences that were entered on the time card and later viewed in Absence Management. Now with the new enhancement, the unpaid break is displayed for the absences entered on the time card as well.

Whenever, the application deducts an unpaid break, it deducts it from the absence duration and displays the break duration in a read only field. This helps users understand how the duration for each absence day was calculated.

The unpaid break field is only displayed if the absence was entered using Redwood pages after the 26B upgrade.

You can now display unpaid break deductions for absences entered on the timecard as well. This help users easily understand how each absence day’s duration is calculated.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · HCM · Absence Management*