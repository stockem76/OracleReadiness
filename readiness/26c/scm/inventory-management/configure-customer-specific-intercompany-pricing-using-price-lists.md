[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# Configure Customer-Specific Intercompany Pricing Using Price Lists

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f49324.htm)

Use the enhanced estimated transfer price service to calculate intercompany transfer prices with customer-specific pricing strategies tied to the referenced sales order fulfillment line. You can now pass the fulfillment line identifier through the estimated transfer price flow so pricing strategies that depend on customer-specific sales order context can return an accurate estimate for shipment and drop ship flows.

You can:

• Pass the sales order fulfillment line identifier into estimated transfer price processing.
• Support customer-specific intercompany pricing strategies that price from the sales order.
• Improve estimated transfer pricing for shipment and drop ship flows.
• Return estimated transfer prices by using the Estimated Transfer Price for Sales Order Shipments REST service.

Here's how it works:

1. Set up customer-specific intercompany pricing with price lists and the required pricing strategy.

2. Call the estimated transfer price REST service for the shipment or drop ship flow.

3. Pass the sales order fulfillment line identifier together with the other required shipment attributes.

4. Let the pricing strategy evaluate the fulfillment line context and return a more accurate estimated transfer price.

You now have an accurate transfer price estimation earlier in the order lifecycle for customer-specific intercompany pricing scenarios. Organizations can generate shipping documentation and review expected transfer prices with a closer match to the sales order pricing context before the actual shipment is created.

## ⚙️ Steps to Enable and Configure

Review the REST service definition in the REST API guides to leverage (available from the Oracle Help Center > *your apps service area of interest* > APIs & Schema). If you are new to Oracle's REST services you may want to begin with the Quick Start section.

## 💡 Tips and Considerations

• In PTO or kit scenarios, the estimated transfer price is computed only for the shippable items.
• The estimated transfer price is returned in the currency defined by the document and accounting rule configuration on the financial flow agreement.
• Agreement identification for transfer price estimation follows the same general process used during actual shipment event enrichment.
• Since the estimate is calculated before the actual transaction, the final accounting transfer price can still differ from the estimated amount returned at order creation time.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains this privilege can access this feature:

• Get Internal Transfer Requesting Organization Price (FOS_INTERNAL_TRANSFER_TRADE_AGREEMENT_SERVICE_GET_REQUESTOR_ORG_PRICE)

This privilege was available prior to this update.

## 📚 Key Resources

Refer to the Oracle Fusion Cloud SCM: *Implementing Manufacturing and Supply Chain Materials Management* guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*