[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Review USOPTE Statutory Tax Rules

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f50308.htm)

We have made it easier for you to review the tax info used by the US Oracle Tax Engine (USOPTE) during payroll processing. Use the Statutory Rules task to view federal, state, and local details in read-only format. Use the Statutory Rules task in My Client Groups to view federal, state, and local details in read-only format.

• Federal income tax (FIT) info for 2019 or earlier W-4 forms and 2020 or later W-4 forms
• Social Security tax rate and wage base details
• Medicare employer and employee rate details
• Federal unemployment (FUTA) tax rate, limit, and credit reduction details
• State income tax (SIT) details, including tax rate tables, deductions, allowances, exemptions, credits, phase-out tables, supplemental rates, and available calculation methods
• State unemployment insurance (SUI), state disability insurance (SDI), paid family and medical leave, Vermont Child Care and Oregon State Transit Tax details
• Local tax details for supported jurisdictions, including partial local criteria and Kentucky local tax contexts

Federal Income Tax Statutory Rules Review

This feature gives payroll professionals a centralized place to verify statutory payroll rule details during payroll calculation review, supplemental payroll review, and tax jurisdiction analysis. It reduces the need to manually search IRS, state, local, or third-party reference material when validating supported statutory tax rates, wage bases, deductions, exemptions, limits, and calculation methods.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• You can filter this content by:
• Legislative data group (LDG)
• Tax category
• Tax type
• Effective as-of date
• W-4 form year
• State
• County
• City
• Other jurisdictional values

The UI displays the rule details that apply to the selected context.

• SIT for OR, AZ, LA, NJ, VA, and MD are outside the scope of this release.
• The statutory rule details displayed depend on the selected tax category, tax type, jurisdiction, effective as-of date, and other applicable criteria.
• Virgin Islands and Guam SIT scenarios follow FIT calculation behavior.

## 🔐 Access Requirements

To access this feature, a user must be assigned a role with these privileges.

• PAY_VIEW_PAYROLL_LEGISLATIVE_UPDATES_PRIV
• PAY_MANAGE_PAYROLL_LEGISLATIVE_UPDATES_PRIV

Payroll Administrator and Payroll Manager are automatically granted these privileges.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*