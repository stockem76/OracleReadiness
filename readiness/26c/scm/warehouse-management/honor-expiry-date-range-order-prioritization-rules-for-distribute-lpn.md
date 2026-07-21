[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Honor Expiry Date Range, Order Prioritization Rules for Distribute LPN

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50161.htm)

Warehouses use flowthrough to move received inventory directly to outbound orders instead of storing it first. When several orders can receive the same inventory, users need a consistent way to decide which inventory should flow through and which order should receive it.

This enhancement lets customers use Crossdock Flowthrough Rules to control flowthrough decisions. WMS can evaluate inventory details, expiry date range, order criteria, and order priority before assigning inventory to an order. This helps customers improve product freshness, reduce manual decisions, and apply the same business rules across receiving and distribution flows.

**RECEIVE BY SHIPMENT/LOAD SUPPORTS FLOWTHROUGH RULES**

Mobile Receive by Shipment now supports the newly added **inventory-orderselection-rule** screen parameter for flowthrough. When this parameter is configured, WMS uses the selected Crossdock Flowthrough Rule to decide whether received inventory should flow through to an order. The rule can include:

• **Inventory Selection Criteria**: When user performs receiving, you can choose which inventories needs to get Flowthrough and which one should be received without performing Flowthrough.
• **Expiry Date Range**: Selection of inventory based on the Expiry range of the inventory.
• **Order Selection Criteria**: Selection of Order which is eligible for Flowthrough.
• **Order Sequence Rule**: When the Flowthrough gets selected, based on which sequence the Flowthrough should happen to select Orders.

WMS evaluates the configured criteria together. If the inventory and order match the rule, WMS performs flowthrough. If the inventory does not match, WMS receives the inventory without flowthrough.

If **inventory-orderselection-rule** is blank, WMS continues to use the existing flowthrough behavior.

**NOTE:** This applies to Mobile Receive by Load transaction flow.

**DISTRIBUTE LPN SUPPORTS FLOWTHROUGH RULES**

Distribute LPN now supports Crossdock Flowthrough Rules for flowthrough decisions. WMS applies the configured rule to evaluate inventory and order eligibility during distribution. This includes expiry date range rules where configured. For Distribution without Residue, WMS follows full LPN allocation behavior. For Distribution with Residue, WMS can allow partial allocation when eligible inventory exists in the LPN.

If **flowthrough-alloc-prty** is configured, WMS also considers it during flowthrough processing.

• Configure Crossdock Flowthrough Rules with the required inventory, expiry date, order, and sequencing criteria.
• Set **inventory-orderselection-rule** on the applicable Mobile flowthrough screens.
• Leave **inventory-orderselection-rule** blank to keep the existing flowthrough behavior.
• Review **flowthrough-alloc-prty** if your flowthrough process uses allocation priority.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*