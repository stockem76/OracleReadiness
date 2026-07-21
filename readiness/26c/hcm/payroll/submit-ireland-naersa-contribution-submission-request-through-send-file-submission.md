[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Submit Ireland NAERSA Contribution Submission Request Through Send File Submission

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f49827.htm)

Use the Ireland Payroll Send File Submission flow to send generated contribution files to NAERSA, monitor processing status, retrieve detailed errors and warnings, and support controlled rollback when needed. Use this feature to:

• Submit generated contribution JSON files to NAERSA from the Send File Submission Process.
• Poll NAERSA processing status and retrieve error details when a submission is not successful.
• Generate two outputs for traceability and reconciliation: 
  • SFS Audit Report
• Errors and Warnings Report
• Route submission processing by flow pattern, including NAERSA MFF Contribution Submission Request.
• Use a rollback override control (RollbackParameterFlag) in the process configuration to allow rollback for specific response scenarios.
• Review submission outcomes in the employer portal, including success, warnings, in-progress, and error outcomes.

To generate the request:

1. Configure the Ireland Revenue web service connection in the process configuration group: -1 for production (Live)
2. Submit Send File Submission Process for Ireland legislative data group.
3. Select NAERSA MFF Contribution Submission Request - Submission ID from the generated request list with optional process configuration group.
4. Review generated output files: 
  1. Audit report
2. Errors and Warnings report

This update adds end-to-end support for NAERSA MyFutureFund contribution submission and follow-up in the Ireland payroll process.

## ⚙️ Steps to Enable and Configure

1. Ensure you've configured the Ireland Revenue web service connection in the process configuration group for production (live)
2. If operational recovery is required, you need to set the Rollback parameter option in the process configuration group according to your rollback policy.

## 💡 Tips and Considerations

• This feature uses existing payroll process security for running Ireland payroll flows.
• Employer portal review and submission actions are performed in MyFutureFund with ROS certificate-based employer access.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*