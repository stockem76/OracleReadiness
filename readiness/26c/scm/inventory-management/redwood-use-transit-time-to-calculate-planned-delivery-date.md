[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# Redwood: Use Transit Time to Calculate Planned Delivery Date

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f46479.htm)

For organizations, accurately projecting when goods will arrive at their destination is critical for planning and downstream operations. In standard scenarios, the Planned Delivery Date on a shipment is derived from the original requested date. This works well when orders and transfers are requested well in advance and shipments occur as expected. However, in real-world situations, such as same-day requests with longer transit times, this approach can result in inaccurate delivery dates. This would lead to misaligned expectations and planning disruptions at the destination location.

You can now calculate the Planned Delivery Date based on transit time and shipping calendars.

When the feature is enabled, the application determines the Planned Delivery Date as follows:

• At shipment creation, the Planned Delivery Date defaults to the requested date from the shipment lines assigned to the shipment.
• Upon shipment confirmation and closure, the Planned Delivery Date is recalculated based on the actual ship date and the transit time defined for the selected ship method.

If the Planned Delivery Date is manually updated before shipment confirmation, the user-entered value is retained and is not recalculated during confirmation. However, if the Planned Delivery Date is cleared prior to confirmation, the application recalculates it at the time of shipment confirmation.

If no ship method or transit time is defined, the Planned Delivery Date defaults to the actual ship date or the requested arrival date, depending on which is later.

Additionally, if a Planned Delivery Date is provided during the Perform Shipping Transaction process (for example, through WMS or third-party logistics integrations), the application uses the provided value and does not override it.

This capability ensures more accurate expected delivery timelines, improving coordination, visibility, and overall supply chain reliability.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Manufacturing and Supply Chain Materials Management*

## 🔐 Access Requirements

Users who are assigned a configured job role that contains this privilege can access this feature:

• Manage Shipments and Shipment Lines (WSH_MANAGE_SHIPMENT_AND_SHIPMENT_LINE_PRIV)

This privilege was available prior to this update.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: *Implementing Manufacturing and Supply Chain Management* guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: *Using Shipping* guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*