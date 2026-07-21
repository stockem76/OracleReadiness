[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# JPK VAT File Updates for Poland 2026 Electronic Invoicing Changes

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49411.htm)

Capture and report transaction classification codes on Payables and Receivables invoices when the KSeF number is either unavailable or to be received at a later date. Keep KSeF numbers and classification codes synchronized across ERP records and Tax Registers.

Add new classification fields to the JPK_V7M(3) layout for taxable unrefunded packaging deposits.

On October 14, 2025, the Polish Ministry of Finance announced updates to the JPK Electronic Audit File VAT Register block, known as JPK_VAT. These updates align JPK_VAT reporting requirements with the mandatory KSeF e-invoicing regulations effective February 1, 2026.

The updates apply to both sales and purchase invoices, and include:

• New indicators DI, BFK, and OFF for transactions processed outside the KSeF system.
• New optional indicators P_360 and K_360 for tax on unrefunded beverage packaging deposits.
• Updated totals for tags *Deklaracja/PozycjeSzczegolowe/P_38* and *Ewidencja/SprzedazCtrl/PodatekNalezny* to include K_360 values.

The enhanced JPK_V7M(3) solution includes these changes:

• New "Non-KSeF" indicator Global Descriptive Flexfields: 
  • The new Non-KSeF Category Global Descriptive Flexfield  stores the non-KSeF category for non-standard invoice processing, values OFF, BFK, or DI, on both the Receivables transaction header and the Payables invoice header. .
• Users can update this field either manually by selecting a value from the list of values or using SOAP Web Services.
• Tax amounts for unrefunded deposits collected for products in beverage packaging, P_360 and K_360. Detailed setup steps are provided below.
• The data model and report XML template are updated to report these values in the JPK_V7M(3) layout.

Business Benefits include:

• Comply with Polish tax authority requirements for the JPK_V7M(3) file.
• Support accurate reporting of tax amounts for unrefunded deposits collected for products in beverage packaging.

## ⚙️ Steps to Enable and Configure

**Setup Steps**

To report tax amounts for unrefunded deposits collected for products in beverage packaging in the P_360 and K_360 tax boxes in the Sales Register, complete this setup for changes effective February 1, 2026.

1. Create Tax Rates for unrefunded deposits transactions collected for products in beverage packaging: 
  1. Navigate to Setup and Maintenance > Manage Tax Rate and Tax Recovery Rates.
2. Create a new tax rate.
3. Associate the tax reporting type and tax reporting codes for Poland.
4. Save your changes.
2. Create the P_360 and K_360 tax reporting codes manually for these tax reporting types:

• ORA_JEPL_VAT_BOXES
• ORA_JEPL_VAT_BOXES_JPK
• ORA_JEPL_VAT_BOXES_PDF

You must enter the codes exactly as shown in the following table:

Tax Reporting Code | Description | Amount Sign | Box Type | Effective Start Date | Effective End Date
P_360 | P_360 | Plus | Recoverable tax box | 01.02.26 | 
K_360 | K_360 | Plus | Recoverable tax box | 01.02.26 |

3. Create new TBA rules with Start Date 01 February 2026 for unrefunded deposits collected for products in beverage packaging transactions. The tax amount for this specific unrefunded deposits transaction should be reported in the Declaration block in the P_360 tag and as standard transaction in the Sales Register in the K_360 tag.

## 💡 Tips and Considerations

• To generate the BFK, DI or OFF tag  in the Sales Register, create a Receivables transaction and a value in the Non-KSeF global descriptive flexfield on the transaction header.
• To generate the BFK, DI or OFF tag  in the Purchase Register, create a Payables Invoice and enter a value in the Non-KSeF global descriptive flexfield on the invoice header.
• To generate transactions in Receivables for unrefunded deposits collected for products in beverage packaging, and report tax amounts in the P_360 and K_360 tax boxes, create a new tax code.

## 🔐 Access Requirements

Assign the Create JPK Extracts for Poland privilege to any duty or job role.

## 📚 Key Resources

Related Help: VAT Registers and JPK Extracts for Poland Topical Essay.

For availability in 26A and 26B, see the Support document ‘Oracle Fusion Cloud ERP: Poland - JPK_VAT Register File update (JPK_V7M(3)), February 2026 (PNEWS2932)’.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*