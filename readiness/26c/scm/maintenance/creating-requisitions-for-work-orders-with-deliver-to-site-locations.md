[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Maintenance](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/maintenance.md)

# Creating requisitions for work orders with deliver-to-site locations

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/maint26c/26C-maintenance-wn-f49540.htm)

This update introduces the new **Deliver-to Site** attribute for locations. **Oracle Purchasing** now validates deliver-to locations in requisitions and purchase orders based on the value of the new deliver-to site attribute. When the Purchasing feature, Restrict Deliver-To Locations to Valid Delivery Sites When Creating Requisitions and Purchase Orders, is enabled, only locations with the **Deliver-to Site** attribute enabled can be used as deliver-to locations in purchase requisitions and purchase orders.

Purchase requisitions can also be created by navigating to **Oracle Fusion Self Service Procurement**from maintenance work orders. In these scenarios, the location associated with the maintenance organization, defined in Inventory organization parameters, is automatically used as the deliver-to location on the purchase requisition. If the maintenance organization location doesn't have the **Deliver-to Site** attribute enabled, the requisition creation for the work order destination may be unsuccessful. To ensure the successful creation of a purchase requisition for a work order, we strongly recommend enabling the maintenance organization location as a deliver-to-site location.

This feature helps requesters and buyers distinguish where goods are received from where they’re delivered, stored, or consumed.

## ⚙️ Steps to Enable and Configure

• Use the **Opt In** page to enable the following feature in **Oracle** **Purchasing**:
• Restrict Deliver-To Locations to Valid Delivery Sites When Creating Requisitions and Purchase Orders

In addition, you must make the **Deliver-to Site** attribute visible in the **Manage Locations** page. Also enable the relevant maintenance organization locations as deliver-to site locations. Refer to the following feature in **Oracle Human Resources** for more details:

• Additional Attributes Deliver-to-Site and Receivable Materials Now Available On Redwood Locations Pages

## 💡 Tips and Considerations

It's mandatory to enable the deliver-to site for maintenance organizations location when the Purchasing feature, Restrict Deliver-To Locations to Valid Delivery Sites When Creating Requisitions and Purchase Orders, is opted in.

**Editing Requisition Lines**

• When the feature is enabled, existing requisitions aren’t affected if they contain deliver-to locations that aren’t marked as deliver-to site locations. However, if users update the deliver-to location while editing a requisition line, they can select only locations that are marked as deliver-to site locations.

**Editing Purchase Orders or Change Orders**

• When the feature is enabled, existing purchase orders and change orders aren't affected even if the current deliver-to location isn’t marked as a deliver-to site location. However, if users update the deliver-to location while editing a purchase order or change order, they can select only locations that are marked as deliver-to site locations.

## 📚 Key Resources

For more information, refer the following features:

• **Oracle Human Resources**
• Additional Attributes Deliver-to-Site and Receivable Materials Now Available On Redwood Locations Pages
• **Oracle Purchasing**
• Restrict Deliver-To Locations to Valid Delivery Sites When Creating Requisitions and Purchase Orders

---
*Oracle Cloud Readiness · 26C · SCM · Maintenance*