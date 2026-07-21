[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Support Substitution and Shorting in Pallet Move Auto Pack Task

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50163.htm)

In high-volume warehouse operations, operators need flexibility to keep packing tasks moving when working with pallets in dynamic floor conditions. The system-allocated pallet for a **Pallet Move Auto Pack task** may not always be the most efficient pallet to use at execution time, especially when another equivalent pallet is more accessible or better suited for immediate processing.

For the 26C release, this enhancement gives operators a more flexible and controlled way to complete pallet move auto pack work. When an eligible homogeneous pallet with the same inventory composition is available, users can substitute it and continue packing without interrupting the workflow. When no suitable substitute is available, users can record the pallet as short directly from the mobile flow, helping ensure the task, allocation, inventory, and downstream processes remain aligned.

By supporting pallet substitution and pallet shorting within the guided Move LPN flow, WMS helps improve operational agility, reduce execution delays, and provide a cleaner process for handling real-world pallet availability scenarios.

As part of this enhancement, we have enhanced WMS to support Pallet Move Auto Pack tasks in the Move LPN mobile flow through:

**SUPPORT SUBSTITUTION PALLET**

For pallet substitution, you can scan an alternate pallet when the allocated pallet is not usable.

• In this release, manual substitution is supported for **Homogeneous** **pallets only**(Pallets containing LPNs with the same SKU and same quantity). The substitute pallet must strictly match the original pallet’s inventory composition, including LPN count, SKU, quantity, batch, expiry, and inventory attributes.

• If validation passes, then system displays a warning message before proceeding with the substitution: 
• If the substitute Pallet is in the same location as the original Pallet : "Do you want to substitute Pallet %s?", then system displays the substitute Pallet# in the message
• If the substitute Pallet is in a different Location/Pallet not Located : "Do you want to substitute Pallet %s from different Location?" - display the substitute Pallet# in the message

• WMS prompts to confirm the substitution and then proceeds with packing. If the substitute pallet is allocated to another PLTMV_AUTOPK task, WMS swaps the allocations as part of the process.

**SUPPORTS PALLET SHORTING**

• For pallet shorting, the Move LPN flow now provides a new hot key “**Ctrl-P: Short Pallet”** on the pallet prompt screen. This is permission-controlled for non-admin users through the existing **Can short picks** group permission.
• On selecting Ctrl-P, the system displays the warning: “Are you sure you want to Short Pallet %s?” 
• If the user rejects the warning, the system returns to the pallet prompt screen without shorting the pallet.
• If accepted, the system proceeds with pallet shorting and follows existing reason code logic based on configured screen and company parameters.

After a successful short, the system displays “No more moves” and returns to the Execute Task selection screen.

**PALLET SHORT UPDATES**

• Shorting the pallet cancels the allocation and the PLTMV_AUTOPK task. 
• When **UPDATE_INVN_ONSHORT** = Yes, then All pallet LPNs are marked as Lost and locked using company parameter LOST_LOCK_CODE.

• LPNs are depalletized, and the pallet is updated to In-Facility with blank Type and Location. 
• When **UPDATE_INVN_ONSHORT** = No, then Pallet/LPNs are deallocated and locked using SHORT_LOCK_CODE.

• The system continues to honour existing order update logic, IHT record creation, and the CC trigger “Short pick full LPN.”

## ⚙️ Steps to Enable and Configure

Ensure the following settings are configured before using the feature:

• Group permission: **Can short picks**is enabled for non-admins.
• Screen parameters for rf.inbound.cwrfmovelpn: prompt-rsncode-onshort, default-reasoncode-onshort, UPDATE_INVN_ONSHORT
• Company parameters: SHORT_REASON_CODE, LOST_LOCK_CODE, SHORT_LOCK_CODE
• Cycle count triggers: Substitute Lpn from different Location, Short pick full LPN
• Order Type setting: Only Deallocate on Short

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*