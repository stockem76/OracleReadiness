[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Payments based on ISO 20022 standard

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f44009.htm)

Use the ISO 20022 (version 2019) payment template to generate International EFT payment files for employees working abroad. The template is enabled through the existing Make EFT process.

Payroll has updated ISO 20022 (2019) compliant template for International EFT payments in UK. When you run Make EFT process (My Client Groups > Payroll > Submit a Flow), the output file format is determined by the Payment Type or Report Category mapping:

• Standard EFT - BACS
• Fast EFT - Faster Payments
• International EFT - ISO 20022

The delivered Extract Delivery Options and Report Category components ensure the ISO 20022 template is correctly linked to International EFT, supporting legislative compliance.

You can use this feature to ensure legislative compliance.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

If you use the ISO 20022 template the first time, please review the steps described in this document 'Steps for moving to ISO 20022 payments for UK Payroll'.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*