[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Procurement](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/procurement.md)

# Redwood: Restrict Supplier Line Access

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/proc26c/26C-procurement-wn-f46445.htm)

Control the access for suppliers to view and respond to specific lines in a negotiation. When creating a negotiation, category managers can restrict supplier access to specific negotiation lines so suppliers only view and respond to the lines relevant to them.

Here are some key enhancements in the Redwood page for this feature over the classic experience:

• Search and filter negotiation lines by item, description, category, or line number to quickly locate specific lines.
• Configure supplier visibility to focus on selected suppliers during review.

Restrict Suppliers Access to Negotiation Lines

Search Lines to Grant or Revoke Supplier Access

Search and Show Suppliers to Grant or Revoke Line Access

Restricting supplier access to negotiation lines gives category managers more control over supplier participation in sourcing events. You can limit each supplier’s visibility to only the lines that are relevant to them, which helps protect sensitive line-level information, provides more clarity about suppliers, and supports more focused responses. This control is especially useful when a negotiation includes many lines or suppliers with different areas of responsibility.

## ⚙️ Steps to Enable and Configure

To use this feature, you must enable these profile options if you haven't already.

• Redwood Pages for Sourcing Enabled (ORA_PON_SOURCING_REDWOOD_ENABLED).
• Redwood Page to Create Negotiation Enabled (ORA_PON_CREATE_NEGOTIATION_REDWOOD_ENABLED)

For instructions on enabling a profile option, refer to the Set Profile Option Values  topic.

## 💡 Tips and Considerations

• By default, only 20 suppliers are displayed on the Restrict Line Access page. If the negotiation has more than 20 suppliers, you can use the Configure Suppliers drawer to search for suppliers and show them on the page, so you can grant or revoke their access to negotiation lines.
• The capability to restrict line access isn’t available for published negotiations when you invite additional suppliers. This capability will be available in a future update.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Create Supplier Negotiation (PON_CREATE_SUPPLIER_NEGOTIATION_PRIV)
• Edit Supplier Negotiation (PON_EDIT_SUPPLIER_NEGOTIATION_PRIV)
• Manage Negotiation Supplier Invitation (PON_MANAGE_NEGOTIATION_SUPPLIER_INVITATION)

These privileges were available prior to this update.

---
*Oracle Cloud Readiness · 26C · SCM · Procurement*