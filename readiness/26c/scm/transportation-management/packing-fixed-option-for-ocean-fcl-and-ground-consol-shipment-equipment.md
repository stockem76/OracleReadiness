[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# Packing Fixed Option for Ocean FCL and Ground Consol Shipment Equipment

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f47378.htm)

This feature allows you to designate specific shipment equipment on your Ground and Ocean FCL consolidated shipments as “packing fixed.” Once marked, the equipment is treated as locked for packing purposes—no additional ship units can be added, and none can be removed. This ensures that preconfigured or physically sealed equipment remains intact throughout planning and execution.

You will find this feature useful in Consol scenarios where certain shipment equipment is preloaded or sealed. In these cases, you must ensure that the contents of that shipment equipment remains unchanged. Previously, there was no straightforward way to prevent the application from adding or removing ship units from a FCL or Ground Consol equipment, which could lead to planning and operational challenges..

In the example below a Ground Schedule Consol shipment with a capacity of two equipment groups will be used to demonstrate the Packing Fixed functionality.

Ground Consol

In this example, three orders will be planned onto a Ground Consol Shipment.  The Packing Fixed option will not be selected in this case - the result will be that the three orders will share one of the Shipment Equipments on the shipment, with the remainder of the third order going into the second Shipment Equipment.

Solution Without Packing Fixed

The Shipment Equipment 2124545466152358, has freight loaded from all three orders -  as shown below.

Shipment Equipment With All Three Orders

The second Shipment Equipment (2124545466152385) holds the balance of the order FIX SEQUIP_GROUND_OR5 as shown below.

Shipment Equipment With Remainder

In the example below, the same three orders will be planned, but in this example the first two orders will be planned into one Shipment Equipment that will then have the Packing Fixed flag turned on, when the Packing Fixed option is selected the Shipment Equipment will be fixed from a packing perspective and ship units will not be added or removed.

Shipment Equipment Two Orders - Packing Fixed

With the Packing Fixed option turned on for the Shipment Equipment 2124545466152358, when the third order is planned on to the Ground Consol, the order will no longer be split with one Ship Unit going to the first Shipment Equipment and remainder going to the second Shipment Equipment, with  Packing Fixed the entire order will be planned into the second Shipment Equipment as shown below.

Packing Fixed on Shipment Equipment 2124545466152358

All three Ship Units for the third order release are now loaded into the second Shipment Equipment.

Third Order Ship Units All Loaded In Second Shipment Equipment

###

**Business Benefit:**This feature provides an approach to prevent changes to your preloaded and/or sealed Consol equipment, eliminating operational issues that can occur if fixed shipment equipment is used for loading additional freight into.

## ⚙️ Steps to Enable and Configure

The Packing Fixed functionality does not require any steps to enable the functionality - the option is available ready to use for your Ground and FCL Consols. To use Packing Fixed option, you will need to edit the desired Shipment Equipment record and check the Packing Fixed option.

1. Navigate to the **Shipment Manager** and open the relevant shipment.
2. Go to the **Equipment** tab or access the **Shipment Equipment Manager**.
3. Select the equipment you want to fix.
4. Select the **Packing Fixed** check box.

The feature is available for:

• Ground Consol shipments
• Ocean (FCL) Consol shipments

No additional system configuration is required.

Shipment Equipment - Packing Fixed Check Box

## 💡 Tips and Considerations

• You can only apply the **Packing Fixed** setting to equipment on supported consol shipments (Ground Consol and Ocean FCL Consol).
• Once enabled, the system prevents all actions that attempt to add or remove ship units from the equipment, including: 
  • Manual packing and repacking
• Shipment merging and splitting
• Bulk planning and order assignment actions
• Fixed equipment is excluded from available capacity calculations. This means it will not be considered for additional load planning or routing decisions.
• Be sure the equipment contents are finalized before enabling this setting, as changes will no longer be allowed afterward.
• The setting is enforced consistently across UI actions, background processes, and integrations.

The actions impacted by the Packing Fixed setting are described below.

Error Message for Disallowed Actions/Changes

All actions that try to remove Shipment Ship Units from Packing Fixed Shipment Equipment will not be allowed with Packing Fixed selected.

This includes:

• Unassign order movement action
• Unassign order release action
• Unassign during bulkplan
• Split shipment by order/order movement/ship unit
• Split planned order release
• Split order movement (new action to allow split reuse and planned order movement)

Actions that try to add Shipment Ship Units to Packing Fixed Shipment Equipment s ship units will not be allowed.

This includes

• Bulkplan order movement/order release
• All build shipment actions for order movement/order releases
• Move order movement/ order release to shipment actions

Actions that change equipment packing:

• Manual Pack Equipment
• Edit load config action
• Merge SSU action
• Merge shipment
• Merge shipment reuse
• Force split merge shipment by s ship units (not on public screen set, deprecated,  we are not making any changes here)
• Force split merge shipment by orders(not on public screen set, deprecated, we are not making any changes here)
• Repack equipment Repack shipment ship unit

**NOTE:**this does not apply to OMD and SMD,  OMD or SMD can still make changes on is_packing_fixed shipment equipment for Ocean FCL Consol or Ground Consol.

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*