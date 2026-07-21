[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# Track Rework Costs Across Standard and Nonstandard Discrete Work Orders

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f49319.htm)

You can now optionally create a new Rework operation in a discrete standard or nonstandard work order to track the costs incurred in rework activities and capture the cost of poor quality for scenarios involving a rework.

Material and resource costs that are incurred in the automatically created rework operation would be tracked separately and aren't included in the cost of products. These costs would be shown in the Rework Amount column on the Work Order Costs page.

Rework Costs Shown Separately in the Work Order Costs Summary

Similarly, all transactions reported in this operation would be shown on the Input Costs tab with a rework indicator.

Transactions in Rework Operation Carry the Rework Indicator

The rework operation created when you move rejected items to rework would also have a rework indicator in the operation-wise summary of the input costs.

Rework Operation Indicator

Scrap and product completions reported in the rework operation would use the costs accumulated till that operation and won't include any rework costs incurred in that operation or any other prior rework operation.

By tracking the rework costs incurred in the rework operations, you can now get improved cost visibility to isolate rework costs and measure the cost of poor quality.

## ⚙️ Steps to Enable and Configure

There are no steps required to enable this feature.

## 💡 Tips and Considerations

• Rework costs are cleared as rework variances when you close the work order. This applies to all the costs methods.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains the following privilege can access this feature:

• Allows review of costs and balances by each individual work order (CST_REVIEW_WORK_ORDER_COSTS_PRIV)

This privilege was available prior to this update.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Using Supply Chain Cost Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*