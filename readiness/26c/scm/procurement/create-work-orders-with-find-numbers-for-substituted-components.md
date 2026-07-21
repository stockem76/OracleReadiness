[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Procurement](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/procurement.md)

# Create Work Orders with Find Numbers for Substituted Components

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/ssproc26c/26C-ssproc-wn-f47246.htm)

Supply Chain Orchestration now supports receiving find numbers for substituted components from Oracle Supply Chain Planning and passing them to Oracle Manufacturing during work order creation.

This enhancement preserves component-specific details when the same item appears multiple times in an item structure with different sequence numbers and is assigned to the same operation.

As a result, work orders can retain find numbers for substituted components, improving visibility when material requirements are consolidated.

Realize the following benefits:

• Receive find numbers for substituted components from Oracle Supply Chain Planning.
• Pass find numbers through Supply Chain Orchestration to Oracle Manufacturing during work order creation.
• Create work orders that include find numbers for substituted components.
• Preserve visibility when the same component appears multiple times within the same operation.

Production operators can retain visibility into repeated or substituted component occurrences within the same operation, and work orders can more accurately reflect the planning details used during their creation.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• This enhancement is applicable when the same component appears multiple times within the same operation.
• Previously, work order creation could consolidate material requirements and ignore material sequence number, reducing operator visibility.

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
• Oracle Supply Chain Planning
• Oracle Manufacturing

---
*Oracle Cloud Readiness · 26C · SCM · Procurement*