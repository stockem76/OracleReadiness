[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Audit Functionality for Costing Setup Pages

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f47242.htm)

You can record and retrieve audit information for the creation, update, and deletion of Oracle HCM Cloud business objects, whether changes are made individually or through bulk upload. The audit functionality tracks changes across multiple costing setup levels, including payroll, element eligibility, department, location, job, position, payroll relationship, assignment, payroll relationship element, payroll assignment element, element entry, and payment source.

Audit reports generated using the **Cost Allocation** business object provide visibility into costing setup changes. Changes to cost allocation accounts appear as insertions because each new costing segment combination creates a new record; these should be interpreted as new combinations rather than updates. To view changes to costed input values in element eligibility, select the **Cost Information** business object type.

Audit is enabled for the following tables:

Table | Business Object Type
pay_cost_allocations_f | Cost Allocation
pay_cost_alloc_accounts | Cost Allocation Account
pay_cost_info_f | Cost Information

This feature improves transparency and financial accuracy by clearly tracking changes to costing data.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 📚 Key Resources

For more information, see Audit Payroll Business Objects.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*