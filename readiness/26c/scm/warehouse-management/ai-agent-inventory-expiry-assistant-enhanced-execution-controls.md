[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# AI Agent: Inventory Expiry Assistant - Enhanced Execution Controls

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f47380.htm)

The **Inventory Expiry Assistant** now supports additional corrective actions for expired outbound and inbound inventory. We've enhanced this agent to handle more questions and be more flexible. Users can take action directly from the agent experience instead of leaving the workflow to manually research and update records.

This enhancement helps reduce the risk of shipping expired inventory by giving warehouse users direct AI Agent actions to isolate or cancel impacted inventory before it moves further through fulfillment.

**The Inventory Expiry Assistant AI Agent now allows you to:**

• Cancel outbound LPNs that are already picked or packed and are at risk of being loaded and shipped by using the bulk cancel OBLPN action through the agent.
• Place holds on allocated or partly allocated inbound tasks through the agent to prevent expired inventory from being packed into outbound LPNs.
• Refresh expired inventory views for reserve and outbound inventory after locking or cancellation actions so you can continue working from current results.

## ⚙️ Steps to Enable and Configure

1. Enable and configure the **Inventory Expiry Assistant AI Agent**capabilities for the applicable users. For more information, see AI Agent Configuration in WMS.
2. Ensure users have permission to perform the underlying bulk cancel OBLPN and bulk hold task actions.

## 📚 Key Resources

See the **AI Agents** section of the **AIML Guide**.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*