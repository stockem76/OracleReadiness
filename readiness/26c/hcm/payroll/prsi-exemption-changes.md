[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# PRSI Exemption Changes

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f49546.htm)

• The PRSI exempt list is refined so it keeps only the three pure exemption categories: A1 Portable Document from EU Member State, Certificate of coverage under Social Security Bilateral Agreement, and Notification of exemption for posted workers.
• Employment of certain family members, Under 16 years of age, Employment on certain social welfare schemes, and Other are no longer treated as pure PRSI exemptions. For these cases, payroll uses Class M with nil liability and insurable weeks instead of omitting the PRSI class.
• Payroll Submission Report, calculation card, and assignment entry handling are aligned so Class M can be used where required, while no PRSI class continues to be reported only for the remaining pure exemption categories.

This change improves the accuracy of PRSI reporting, helps downstream agencies identify why an employee is exempt, and supports cases where benefit eligibility depends on the recorded PRSI class, such as Under 16 scenarios for Occupational Injuries Benefit.

## ⚙️ Steps to Enable and Configure

• Review employments that currently use Employment of certain family members, Under 16 years of age, Employment on certain social welfare schemes, or Other as PRSI exempt reasons.
• For affected records, use Class M with nil liability and insurable weeks instead of treating these cases as pure PRSI exemptions.
• Continue to use no PRSI class only for the three pure exemption categories that remain in the PRSI exempt list.

## 💡 Tips and Considerations

• Existing users may already have employments that use one of the four reasons removed from the PRSI exempt list.
• The three pure exemption categories remain PRSI exempt and continue without PRSI class reporting.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*