[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Maintenance](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/maintenance.md)

# Redwood: Update Preventive Maintenance Service Requests and Work Orders for Changes in Associated Maintenance Plan

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/maint26c/26C-maintenance-wn-f46521.htm)

The Create Service Work Orders for Preventive Maintenance process now supports maintenance work order cancellations.

When a preventive maintenance work order is canceled in Oracle Maintenance Cloud, the process updates the related service requests and service work orders statuses. Each time the job runs, it identifies canceled maintenance work orders that are linked to open service requests and syncs the related service requests and service work orders.

The job now creates Fusion Field Service work orders, in addition to the existing generic work orders and Oracle Field Service Cloud work orders.

Create Service Work Orders for Preventive Maintenance ESS Job

By allowing Oracle Fusion Service Cloud to stay in sync when preventive maintenance work orders are updated in Maintenance Cloud, this feature helps teams better manage changes to asset service work and maintain accurate data across preventive service planning and execution.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

The Fusion Field Service Work Orders are created only in Draft status now by the ESS Job.

---
*Oracle Cloud Readiness · 26C · SCM · Maintenance*