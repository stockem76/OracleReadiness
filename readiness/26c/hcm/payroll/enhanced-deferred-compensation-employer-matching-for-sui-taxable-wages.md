[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Enhanced Deferred Compensation Employer Matching for SUI Taxable Wages

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f49874.htm)

We have enhanced our deferred-compensation contributions processing with the addition of elements that support state unemployment insurance (SUI) wage treatment for states where employer-matching contributions must be included in SUI taxable wages. We have updated the deferred compensation plan element templates to include this option. All employer-match indirect elements created by the templates will use the new Employer Contributions classification and Deferred Compensation Employer Match secondary classification.

Primary classification | Employer Contributions
Secondary classification | Deferred Compensation Employer Match
Plan types | 401 (k), 403 (b), 457 (b)
SUI states | Arizona, California, Illinois, Massachusetts

Employee contribution elements aren’t impacted.

• Only elements defined through the updated template will have their employer-match amounts evaluated for SUI wages.
• Employer-match amounts from multiple deferred compensation sources, such as pretax and Roth contributions, are evaluated together for SUI wage purposes.
• Supports state SUI compliance for employer-matching contributions in Arizona, California, Illinois, and Massachusetts.
• Reduces manual configuration and workarounds for SUI wage reporting.
• Preserves federal wage treatment for employer matching contributions.
• Keeps employer match reporting aligned with existing Employer Charges reporting.
• Supports consistent SUI wage evaluation when employer match is calculated from multiple contribution sources.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• This feature applies to these states.
• Arizona
• California
• Illinois
• Massachusetts

Employer-matching contributions remain excluded from SUI wages by default for all other states.

• Only elements defined through the updated template will have their employer-match amounts evaluated for SUI wages.
• Employer-match amounts from multiple deferred compensation sources, such as pretax and Roth contributions, are evaluated together for SUI wage purposes.
• To use this feature, you must deprecate your older elements and redefine them. It’s strongly recommended that you transition all employer-match elements for a plan to the new model at the start of a new plan year or calendar year.
• Don’t use legacy employer-match elements and new employer-match elements together for the same payroll processing model. Payroll processing is blocked when mixed employer match configurations are detected.
• Employer-matching contributions remain excluded from federal income tax (FIT), Social Security, Medicare, and Federal Unemployment Tax Act (FUTA) wages.
• Employer matching contributions continue to appear in employer-side reporting under Employer Charges.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*