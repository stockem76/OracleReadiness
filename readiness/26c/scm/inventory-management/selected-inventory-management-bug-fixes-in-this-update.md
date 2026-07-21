[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# Selected Inventory Management Bug Fixes in This Update

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f49931.htm)

This update includes some bug fixes that can change the way Oracle Inventory Management works. This isn't a full list of all the bug fixes in this update. This list includes the bug fixes that can cause a noticeable change in application behavior.

**View More Serial Numbers Associated with Inventory Lots on Transaction History Page**

With this update, the Transaction History page has been enhanced with a separate tab to show all serial numbers associated with an inventory lot. Prior to this update, only the first 25 associated serial numbers were shown for a lot.

Oracle reference: 39077798

**Convert UOMs on Redwood Pages for Cycle Counts and Physical Inventories**

With this update, a new collapsible UOM Conversions section is now available on the Record Cycle Count, Mobile Cycle Count, Mobile Physical Inventory, and Physical Inventory Spreadsheet flows. The section is hidden and collapsed by default. It can be enabled using the UOM Conversions Section business rule and can be expanded by users as needed.

Oracle reference: 39410883

**Update Account and Requestor Search Behavior on Redwood Movement Request Page**

Prior to this update, users could search the Redwood Movement Request page by entering any part of a value. For example, in the **Requestor** field, entering a last name returned any requestor whose full name contained that text. With this update, the search now uses a **starts with** match to improve performance, so users must enter the beginning of the name. To perform a **contains** search, enter **%** on both sides of the value. In addition, with this update the list of values no longer sorts by name or account number.

Oracle reference: 39333067

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*