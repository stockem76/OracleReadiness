[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Usability Enhancement for Organization Calculation Cards

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f50370.htm)

We have made it easier for you to manage the info in your organization calculation cards, including:

• Definingfederal and regional tax rules in a consolidated user interface
• Managing enforcement of pretax deduction annual compensation limit
• Defining tax groups and managing TRU associations

For more information, see What are organization calculation cards for the US?

• Users can manage all federal tax overrides in a single page.
• Users can manage all state tax overrides in a single page.

## ⚙️ Steps to Enable and Configure

To enable any Redwood page in 26C, set the **ORA_HCM_VBCS_PWA_ENABLED** central profile option to **Y** (Enable VBCS Progressive Web Application User Interfaces across HCM application).

## 💡 Tips and Considerations

This enhancement may impact your HCM Data Loader (HDL) scripts. Review your scripts and make these changes.

• For Federal Income Tax DAT files, replace **Federal Income Tax**with **Federal taxes**.
• For State Income Tax DAT files, replace **State Income Tax**with **State taxes**.

## 📚 Key Resources

https://docs.oracle.com/en/cloud/saas/human-resources/fapus/what-are-organization-calculation-cards-for-the-us.html

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*