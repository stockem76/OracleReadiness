[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Apply Default Lock Code for Inventory Discrepancy in Outbound Audit

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50166.htm)

This enhancement helps warehouse operations to handle outbound audit discrepancies more consistently. When an auditor finds an extra inventory during a non-simulated outbound LPN audit, WMS can now automatically place the LPN on hold using a configured lock code. This reduces manual decisions during audit completion and helps prevent LPNs with known discrepancies from being shipped.

**DEFAULT LOCK CODE FOR INVENTORY DISCREPANCY**

In 26C, WMS improves the Outbound Audit flow for outbound LPN audits by introducing a new  screen parameter for Outbound Audit:

• New parameter: **default-lockcode-for-invn-discrepancy**
• Screen: rf.outbound.cwrfauditlpnplt
• Default value for existing screens: Blank

When users perform a non-simulated outbound LPN audit and end the audit with a positive inventory discrepancy, WMS can automatically apply the configured default lock code to the LPN.

This applies when the auditor records an extra quantity for an expected item, an unexpected item in the LPN, or an expected item with unexpected inventory details, such as batch, expiry, or inventory attributes.

When the above conditions are fulfilled at End Audit, "**default-lockcode-for-invn-discrepancy**" takes precedence over existing "**prompt-lockcode-for-invn-discrepancy**" as follows:

default-lockcode-for-invn-discrepancy | prompt-lockcode-for-invn-discrepancy | Result
Set with a valid Lock Code | Yes / No / Blank | WMS applies it automatically and does not prompt the user to select a lock code
Set with invalid Lock code | Yes / No / Blank | WMS displays a message "Invalid Default Lock Code for Inventory Discrepancy. Configure a valid Lock code to proceed". On accepting, the system will display only the active and valid Lock codes. You can select a Lock code from the displayed list to proceed with the transaction.
Blank | Yes | WMS continues to display "Apply lock code to end Audit?"; on proceeding, system prompts for lock code selection, then proceed by selecting lock code to the OBLPN.
Blank | <Blank> / No | WMS continues to use the existing prompt-lockcode-for-invn-discrepancy behaviour.

**NOTE:** This does not apply to simulated outbound LPN audits.

**ENHANCEMENTS TO OUTBOUND AUDIT WARNING MESSAGES**

As part of this enhancement, WMS now also improves several Outbound Audit warning messages in the Outbound Audit flow. These messages are clearer and follow the enable or disable settings in Message Configuration.

Audit OBLPN Scenario | Warning Messages | Previous  Behaviour | Improvements Made
After scanning an unanticipated Batch/Expiry/Attribute value. | “Scanned SKU/inventory combination does not exist, record discrepancy ?” | Even if this message is disabled, the system still displays it in the screen flow. | Now, warning messages for unexpected item, quantity, batch, expiry, or inventory attribute discrepancies can be enabled or disabled based on business needs.
After scanning: An extra quantity for an anticipated Batch/Expiry/Attribute inventory, or a quantity for an unanticipated Batch/Expiry/Attribute inventory. | Mismatch in %s for %s and inventory batch/Expiry/Attribute combination. Proceed further? | Even if this message is disabled, the system still displays it in the screen flow. | Now, warning messages for an anticipated Batch/Expiry/Attribute inventory, attribute discrepancies can be enabled or disabled based on business needs.
After scanning SKU/SKU-Qty for an unanticipated SKU. | Item does not exist in LPN %s %s. Record discrepancy? | Even if this message is disabled, the system still displays it in the screen flow. | You can now enable/disable this warning message based on business needs. The item discrepancy message is reworded as following to clearly show the item and LPN. "Item %s does not exist in LPN %s. Record discrepancy?", where the first %s is the SKU and the second %s is the LPN# .
After scanning extra quantity for normal inventory. | Mismatch in Qty for SKUs %s. Proceed further? | This is hard-coded. | A previously hard-coded quantity mismatch warning is now configurable and enabled, by default.
If discrepancies are found for any anticipated or unanticipated SKU, and upon accepting End Audit. | Mismatch in %s for %s and inventory batch/expiry/attribute combination. Do you want to adjust LPN? | This message is displayed in both simultaneous and non-simultaneous mode. This message is displayed even if the audit does not result in an LPN inventory update. | The discrepancy message is now reworded as follows to use clearer action text. "Mismatch in %s for %s and inventory batch/expiry/attribute combination. Proceed?" You can now enable/disable this warning message only based on business needs.

## ⚙️ Steps to Enable and Configure

1. Go to the **Mobile Outbound Audit screen** configuration for rf.outbound.cwrfauditlpnplt.
2. Set audit-mode to **blank**.
3. Set**default-lockcode-for-invn-discrepancy** with a valid lock code.
4. Review **prompt-lockcode-for-invn-discrepancy** and configure it based on whether users should manually select a lock code when no default lock code is configured.

**NOTE**: When the configured default lock code is invalid, the system displays a message and requires the user to select a valid lock code to complete End Audit.

1. In Message Configuration UI, review the **Outbound Audit** warning messages and enable or disable them based on your business process.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*