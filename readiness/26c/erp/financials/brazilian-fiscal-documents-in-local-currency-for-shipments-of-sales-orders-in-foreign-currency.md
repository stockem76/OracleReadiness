[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Brazilian Fiscal Documents in Local Currency for Shipments of Sales Orders in Foreign Currency

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49373.htm)

Generate and report fiscal documents in Brazilian Real for shipments associated with sales orders entered in foreign currency. The process automatically converts foreign currency amounts to the local currency and displays the converted values on the Fiscal Document page and in the XML sent to the tax authority.

If a fiscal document requires reprocessing due to validation errors, tax information can be recalculated after updating tax determinants or conversion rates. The application validates the required currency conversion data and raises validation errors when conversion information is missing or incomplete.

For export transactions, specify the currency conversion rate negotiated with the exported broker and bank in the Fiscal Attributes page or in the Import Outbound Fiscal Document FBDI.

Fiscal Attributes page

The currency exchange is always from the sales order currency to Brazilian Real. The currency conversion rate specified in the fiscal attributes is also applied to the corresponding Receivables transaction created from the sales order. In Brazilian foreign currency sales order flows, the sales order currency conversion rate is for quoting purposes only.

Business benefit includes ensuring compliance with Brazilian tax authority regulations by generating fiscal documents in the required local currency, regardless of the sales order currency.

## ⚙️ Steps to Enable and Configure

To enable the feature, follow these steps.

1. In the Setup and Maintenance work area, click the Task icon and select the Search menu option.
2. Search Manage Standard Lookups task and click on it.
3. In the Search section on the Manage Standard Lookups page, enter ORA_ERP_CONTROLLED_CONFIG in the Lookup Type field and click Search.
4. If the JL_ENABLE_FEATURE lookup type does not exist, create the lookup type. Click the New (+) icon to add the lookup type. 
  1. In the Lookup Type field, enter ORA_ERP_CONTROLLED_CONFIG.
2. In the Meaning field, enter Controlled feature or enhancement.
3. In the Description field, enter ORA_ERP_CONTROLLED_CONFIG.
4. In the Module field dropdown, select Shared.
5. Click Save or Save and Close.
5. In the ORA_ERP_CONTROLLED_CONFIG: Lookup Codes section, click the New (+) icon to add lookup code JG_35500622.
6. Enable the Lookup code and select the Start Date.
7. In the Meaning and Description field, enter JG_35500622.
8. Click Save or Save and Close.

## 💡 Tips and Considerations

• Activate the feature by enabling the corresponding lookup. If the lookup isn’t enabled, the application continues to block fiscal document requests for shipments originating from sales orders in currencies other than Brazilian Real.
• The feature is restricted to sales order shipments.
• Enter a valid currency conversion rate and conversion date in the fiscal attributes. The application raises a validation error if either value is missing.
• The feature supports tax recalculation for fiscal documents previously rejected by the tax authority. Updates to tax determinants or currency conversion rates automatically trigger a tax re-evaluation during reprocessing.

## 🔐 Access Requirements

No new access requirements.

## 📚 Key Resources

Based on Idea 626754 from the Idea Lab on Oracle Cloud Customer Connect.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*