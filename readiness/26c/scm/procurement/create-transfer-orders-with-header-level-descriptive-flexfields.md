[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Procurement](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/procurement.md)

# Create Transfer Orders with Header Level Descriptive Flexfields

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/proc26c/26C-procurement-wn-f47247.htm)

Use the Oracle Supply Chain Orchestration Supply Requests REST API and the Supply Order Import FBDI template to create transfer orders with header level descriptive flexfields.

Oracle Supply Chain Orchestration now supports transfer order header-level descriptive flexfields in the Supply Requests REST API and the Supply Order Import FBDI template. When you create a transfer order through either integration path, Supply Chain Orchestration passes the header-level descriptive flexfield values to Oracle Inventory Management, which creates the transfer order with those values.

Realize these benefits:

• Include transfer order header-level descriptive flexfield values in Supply Requests REST API payloads.
• Include transfer order header-level descriptive flexfield values in Supply Order Import FBDI imports.
• Pass a common set of transfer order header attributes to downstream third-party systems.

You can maintain a common set of transfer order header attributes and pass them to downstream third-party systems when creating transfer orders through integrations.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• This enhancement adds support for transfer order header-level descriptive flexfields.
• Support for transfer order line-level descriptive flexfields was already available.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Process Supply Order Interface (DOS_PROCESS_SUPPLY_ORDER_INTERFACE_PRIV)
• View Supply Orders (DOS_VIEW_SUPPLY_ORDERS_PRIV)
• Manage Supply Request Exceptions (DOS_MANAGE_SUPPLY_REQUEST_EXCEPTIONS_PRIV)
• View Supply Order Exceptions and Status (DOS_VIEW_SUPPLY_ORDER_EXCEPTIONS_AND_STATUS_PRIV)

These privileges were available prior to this update.

## 📚 Key Resources

• Overview of Setting Up Supply Chain Orchestration
• Using Supply Chain Orchestration
• Supply Requests REST API
• Supply Order Import FBDI template

---
*Oracle Cloud Readiness · 26C · SCM · Procurement*