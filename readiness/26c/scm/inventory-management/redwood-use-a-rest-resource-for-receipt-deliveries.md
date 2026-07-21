[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# Redwood: Use a REST Resource for Receipt Deliveries

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f46477.htm)

When you handoff goods to PAR locations, satellite locations, or end requesters using receipt deliveries, it ensures that supplies reach their intended destination accurately and on time. However, without standardized integration points, managing, updating, or tracking these deliveries across systems can be fragmented and inefficient when relying on external systems or partner applications to manage last-mile inventory processes.

Now, you can use the Receipt Deliveries REST resource to create an ad hoc delivery and to view, complete, update, or cancel existing receipt deliveries.

The Receipt Deliveries REST resource supports the following actions:

• Create ad hoc deliveries
• Find and view deliveries
• Add deliveries to a cart or remove them from a cart
• Complete one or multiple deliveries
• Cancel one or multiple deliveries

This feature allows you to streamline last-mile delivery workflows, improve visibility into delivery status, and ensure greater accuracy and control over how goods are distributed to their final destinations.

## ⚙️ Steps to Enable and Configure

Review the REST service definition in the REST API guides to leverage (available from the Oracle Help Center > *your apps service area of interest* > APIs & Schema). If you are new to Oracle's REST services you may want to begin with the Quick Start section.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains this privilege can access this feature:

• Perform Receiving Receipt Transaction by Web Service (RCV_PERFORM_RECEIVING_RECEIPT_TRANSACTION_WEB_SERVICE_PRIV)

This privilege was available prior to this update.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: REST API for Oracle Fusion Cloud SCM guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*