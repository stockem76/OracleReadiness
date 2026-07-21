[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Absence Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/absence-management.md)

# Compensatory Time Interface Enhancements

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/amg-26c/26C-absence-mgmt-wn-f49554.htm)

Two new enhancements to the compensatory time integration are being introduced in this release.

• **Entry-Level Approval Support for Payroll Users**

   Previously, when the **Update Compensatory Plan Balance** option on the Absence Management Job Configuration page was set to **On timecard approval,** any compensatory time earned—whether entered directly on the time card or created through time calculation rules—was sent to **Absence Management** after the time card was approved. This happened regardless of whether the customer used the **Timecard Approval BPM** task or the **Entry Level Approval (ELA) BPM** task.

With this enhancement, when customers use the **Timecard Approval ELA** task, compensatory time earned entries are now sent to **Absence Management** as soon as each individual time entry is approved. As compensatory time moves from **Time and Labor** to **Absence Management**, the **Compensatory Plan Balance** is updated right away, so the employee can use the time immediately.

The deleted time entries do not go through entry-level approval. Because of this, deleted entries are subtracted from the **Compensatory Plan Balance** only after the entire timecard is approved.

• **Compensatory Time Capabilities Extended to Project-Only Users**

Customers who use only Project modules and third-party payroll systems can now use the Compensatory Time features in Time and Labor and Absence Management. By configuring the **Update Compensatory Plan Balance** option on the Absence Management Job Configuration page, users can choose when **Compensatory Time Earned** is sent to **Absence Management**—either when the time card is submitted or after it is approved.

• If the option is set to **On timecard submission,** the compensatory time, whether entered manually or created through rules, is sent to **Absence Management** when the time card status changes to **Submitted**.
• If the option is set to **On timecard approval** and the **Project Time Card Approval BPM** task is used, the time is sent when the time card status changes to **Approved**.

When the **Project Timecard Approval ELA BPM** task is used, compensatory time is sent to **Absence Management** as each individual entry is approved.

If compensatory time is entered or created by time calculation rules without project attributes, the compensatory time entry is automatically approved after all project entries are approved and the time card status is updated to **Approved**. Deleted compensatory time is also removed from the absence plan balance when the entire timecard status is updated to **Approved**.

For customers using both **Payroll** and **Project** modules, **compensatory time** will continue to follow the **Payroll Consumer** rules.

Improve compensatory time processing with entry-level approvals that sync approved time directly to Absence Management. Additionally, project-only customers using third-party payroll systems can now utilize compensatory time features.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · HCM · Absence Management*