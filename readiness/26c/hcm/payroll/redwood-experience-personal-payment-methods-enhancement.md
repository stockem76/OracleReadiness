[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Redwood Experience: Personal Payment Methods Enhancement

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f49859.htm)

You can now update the account holder’s name in a bank account even after the account has been used in a payment process. You can edit the account holder’s name and save the changes, while all other fields remain disabled after payments are processed. This enhancement is available in both the self-service and professional user experiences.

This enhancement ensures that payments do not fail due to differences in the account holder's name.

## ⚙️ Steps to Enable and Configure

An administrator can set up this feature by enabling the switch:

1. Go to **Setup and Maintenance > Tasks panel > Search > Manage Standard Lookups**.
2. Search for the **ORA_ERP_CONTROLLED_CONFIG** lookup type.
3. Create a lookup code as **IBY_36266854**, with meaning and description as **Update bank account name used in payroll**.
4. Save the changes.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*