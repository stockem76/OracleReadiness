[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Dynamic Federal and Provincial Tax Exemption

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f50351.htm)

This enhancement introduces support for exempting Federal and/or Quebec Provincial Income Tax calculations through template formula configuration.

To support this functionality, the following Work Storage Area (WSA) variables are now available during payroll processing:

• CA_DYN_FIT_EXEMPT – Exempts Federal Income Tax calculation

• CA_DYN_PIT_EXEMPT – Exempts Quebec Provincial Income Tax calculation

The formula for any assignment level element processed in the payroll run can be modified so that under certain conditions any of the above variables is set to Y. This will ensure that the employee is exempted from Federal Income Tax and/or Provincial Income Tax.

**Formula Logic**

DEFAULT FOR CA_GET_STATUTORY_REPORTING_TYPE IS ' ' 

l_payroll_rel_action_id = GET_CONTEXT (PAYROLL_REL_ACTION_ID, 0) 

l_tax_unit_id = GET_CONTEXT(TAX_UNIT_ID,0) 

l_reporting_type = CA_GET_STATUTORY_REPORTING_TYPE 

l_dyn_exempt_key = to_char(l_payroll_rel_action_id)||'_'||to_char(l_tax_unit_id)||'_'||l_reporting_type 

IF (Percentage = 100 AND l_pretax_iterate_flag = 'Y') THEN 

( 

   WSA_SET(to_char((l_dyn_exempt_key||'_CA_DYN_FIT_EXEMPT','Y') 

   WSA_SET(to_char((l_dyn_exempt_key||'_CA_DYN_PIT_EXEMPT','Y') 

)

This enhancement provides flexibility in configuring Federal and Quebec Provincial Income Tax exemptions.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• The logic only works for assignment-level elements.

• An IF condition defines the criteria under which the tax exemption is applied.

• The formula must reference the payroll relationship action ID, tax unit ID and reporting type. If the formula doesn't already include these references, the following must be added to the code:

• Payroll relationship action ID: I_payroll_rel_action_id = GET_CONTEXT (PAYROLL_REL_ACTION_ID, 0)

• Tax unit ID: I_tax_unit_id = GET_CONTEXT(TAX_UNIT_ID,0)

• Reporting type: l_reporting_type = CA_GET_STATUTORY_REPORTING_TYPE

## 📚 Key Resources

Refer to these documents on the Canada Information Center for additional information.

Canada Information Center: https://support.oracle.com/support/?anchorId=&documentId=KA144

• CA – Payroll tab > Product Documentation > Payroll Guides > Administering Payroll for Canada

Help Center: https://docs.oracle.com/en/cloud/saas/human-resources/oapff/index.html

• Cloud > Cloud Applications > Human Resources > Administering Fast Formulas

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*