[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Human Resources](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/human-resources.md)

# Perform a Baseline Extraction of Payroll Interface for ADP Workforce Now

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hure-26c/26C-hr-wn-f49857.htm)

Perform a baseline extraction for Payroll Interface for ADP Workforce Now to ensure that a full file doesn't get extracted after uptaking this update.

Route changes have been delivered to relax time periods join at the 3rd level (to avoid employees getting picked up even if no time periods are present). Further, the threading level join (period_type = 'E') has been removed and has been incorporated as filer criteria.

**NOTE**: You should perform a baseline extraction after applying this patch to avoid a full file extraction.

Perform regular data changes and extractions after the baseline extraction.

This ensures that a full file doesn't get extracted in the Payroll Interface for ADP Workforce Now.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · HCM · Human Resources*