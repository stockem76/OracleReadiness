[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Assign and Unassign Orders from Outbound Load Number Orders

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50175.htm)

Outbound Load UI now enables users to assign orders directly from the load details screen, providing a faster and more intuitive workflow. This simplifies load management, reduces manual steps, and improves operational efficiency when assigning orders to outbound loads.

A new button **Assign Order**is introduced in the **Outbound Load -> Number Orders UI**. Users can use this button with permission new permission **load / can assign order** enabled.

Users can search and select one or more eligible orders. After assignment, WMS updates the load’s number of orders and OBLPNs. WMS also supports removing assigned orders through Unassign Order.

**NOTE:** Orders that are already assigned to another load are not reassigned, and the system displays the reason.

Now, the Redwood **Outbound Load**-> **Number Orders**UI supports Advanced Search when assigning orders. Users can search for orders using advanced criteria and WMS filters the order results based on the search conditions before assignment.

## ⚙️ Steps to Enable and Configure

To Assign and Unassign orders from the **Outbound Load -> Number Orders**UI:

1. Grant the load / can assign order permission to the required user groups.
2. Open the OB Load and go to Num Orders.
3. Use Assign Order to search and add eligible orders to the load.
4. Use Unassign Order to remove orders when needed.
5. Review warnings for orders associated with external planned loads.

To search Assign Order from the Redwood **Outbound Loads**UI:

1. Confirm users have access to the Assign Order action.
2. Open Redwood OB Load and go to Num Orders.
3. Use Advanced Search to find eligible orders.
4. Select and assign the required orders to the load.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*