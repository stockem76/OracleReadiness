[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Absence Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/absence-management.md)

# Optional Reason for Discretionary Disbursements

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/amg-26c/26C-absence-mgmt-wn-f49553.htm)

You can now configure absence plans to mandate reason selection when disbursing balances. You can define your list of acceptable reasons using the new ANC_DISBURSEMENT_REASONS lookup code. You need to attach these reasons to the specific absence plan in the Discretionary Disbursements section of the setup page. Once the reasons are linked to the plan, users need to select a reason whenever they enter or upload disbursement transactions through HDL.

Once you enable reason selection, a new **Reason**field is displayed on the Cash Disbursements Redwood page as well as the Absences and Entitlements Redwood page. When a disbursement reason is selected, it gets displayed on the Cash Disbursement list view and the Plan Balance Details sections. Administrator see the reason in the Update balance details drawer within the Absences and Entitlements page.

If approval workflows are enabled for disbursement transactions, the disbursement reason will be included in the approval notification. Additionally, the Plan Balance REST service has been updated to return disbursement reasons when retrieving balance details.

You can now ensure that balance disbursement is captured with a clear reason for better tracking and compliance. Give organizations more control and transparency over absence plan disbursements.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · HCM · Absence Management*