[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Partner E-Invoice Integration with Thomson Reuters for France

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f50408.htm)

France has mandated e-invoicing and reporting requirements to modernize tax administration, and simplify business-to-business billing. The mandate includes electronic exchange of invoices in structured format between businesses, automatic rejections and reporting of self-billed and cross-border invoices.

Release 26B introduced a turnkey onboarding solution for e-invoicing integration with Thomson Reuters. In this release, businesses can comply with the French mandates by reporting self-billed and cross-border invoices through Thomson Reuters integration. The Payables Invoice and Life Cycle Status Extract for France process is enhanced to transmit the transaction details to Thomson Reuters, when the partner e-invoice integration is enabled. Thomson Reuters submits the transaction details to the tax authorities.

The business benefit of this feature is that it helps businesses comply with the regulatory mandates for France, leveraging the partner e-invoice integration with Thomson Reuters.

## ⚙️ Steps to Enable and Configure

• Enable partner e-invoice integration service using the setup task “Manage Thomson Reuters Services”. For details on this task, refer to the Partner E-invoice Integration with Thomson Reuters
• You can enable e-invoicing for Payables and Receivables and select the legal entities for Receivables e-invoicing.
• Submit the Payables Invoice and Life Cycle Status Extract for France process by selecting the legal entity and the time period for which you want to generate the report.

## 💡 Tips and Considerations

• This feature enhances the existing Payables Invoice and Life Cycle Status Extract for France process to check whether partner e-invoicing is enabled for the selected legal entity and automatically route the report to the correct end point.
• Ensure that you enable the legal entities in Receivables e-invoicing activation.

## 🔐 Access Requirements

You must have the Manage Thomson Reuters Services privilege to establish connectivity with Thomson Reuters and select the legal entities for activation.

## 📚 Key Resources

• Guidelines for Configuring Security in Oracle ERP Cloud
• Partner E-Invoice Integration with Thomson Reuters

---
*Oracle Cloud Readiness · 26C · ERP · Financials*