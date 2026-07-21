[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Order Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/order-management.md)

# Redwood: Attach Subscription or Coverage Line to Existing Subscription

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/order26c/26C-order-mgmt-wn-f46423.htm)

Order entry users can save time and reduce errors by specifying an existing subscription on subscription or coverage lines in the Redwood sales order experience, including the sales order line, Manage Subscriptions and Coverages tab, and subscription or coverage drawers. The target subscription value is also supported through REST services, REST-based stage order services, and FBDI, so upstream and imported orders can carry the same instruction.

**Get these benefits**

This feature helps optimize order entry processes by keeping add-on subscription and coverage purchases on the customer intended subscription, reducing fragmented subscriptions, billing and renewal misalignment, entitlement or coverage issues, and manual correction work. It also improves subscription data quality for reporting on ARR, renewals, customer holdings, and product adoption.

**How it works**

When a target subscription is provided, the line is added to the specified subscription. Grouping conditions are ignored for that line. The application validates that the target subscription has the same customer or primary party, business unit, legal entity, and currency.

The Attach to Subscription value is copied or retained in supported copy and revise flows and is re-validated at submit. For coverage and model structures, the value cascades to child coverage or model lines when applicable.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Sales*

You must opt in to these features:

• Order Management > Order Management > Redwood: Create and Manage Sales Orders
• Sales > Subscriptions >  Integrate Order Management with Subscription Management  
  • Integrate Order Management with Subscription Management to Process Subscriptions
• Integrate Order Management with Subscription Management to Process Coverages

## 💡 Tips and Considerations

• Only target subscriptions with the same customer or primary party, business unit, legal entity, and currency are valid.
• If the target subscription is invalid, nonexistent, or ineligible, the transaction or import row returns an error instead of silently creating a separate subscription.
• The ADF order experience does not show this field, but if passed in background it will be honored.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature in the Order Management work area:

• Initiate Order (FOM_CREATE_ORDER_PRIV)
• Revise Order (FOM_REVISE_ORDER_PRIV)
• Monitor Sales Order (DOO_MONITOR_SALES_ORDER_PRIV)
• Update Order Pricing Details (FOM_UPDATE_PRICING_DETAILS_PRIV)

## 📚 Key Resources

• Set Up Coverages and Subscriptions for Sales Orders

---
*Oracle Cloud Readiness · 26C · SCM · Order Management*