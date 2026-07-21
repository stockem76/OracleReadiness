[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Sales and Operations Planning](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/sales-and-operations-planning.md)

# Apply Time-Phased Safety Stock Smoothing and Rounding Across Echelons

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/sop26c/26C-sales-ops-wn-f45785.htm)

You can now stabilize safety stock targets across multiple supply chain echelons by smoothing safety stock levels over defined time intervals and limiting fluctuations between periods. Safety stock values are automatically rounded up to the nearest whole number and rounding adjustments propagate through the bill of materials and sourcing network. Child safety stock is adjusted based on parent rounding offsets, with the square root of sum of squares logic applied for items with multiple parents to maintain statistical accuracy and preserve service levels.

With this update, you can reduce erratic safety stock fluctuations to stabilize inventory targets across the supply chain. It improves operational efficiency by minimizing frequent minor stock adjustments. It also increases service levels and prevents stockouts through consistent integer-based safety stock rounding.

Oracle Inventory Optimization Planning calculates time-phased safety stock values across the planning horizon. However, there may be frequent changes to the safety stock if the demand variability is high. Inventory Optimization Planning allows for smoothing this variability in two ways:

• Enables you to hold a constant safety stock for a specified interval in the planning horizon
• Enables you to limit the variations from one interval to the next to avoid spikes

You can use the following plan-level options in Plan Options to control the stability of the safety stock:

• Safety Stock Change Interval in Days
• Maximum Percentage Variation in Safety Stock Values

Safety Stock Parameters in Plan Options

The interval specified in days is always converted to a whole number of weeks. So, if the manufacturing calendar is a 5-day week calendar, 12 days will be rounded up to 3 weeks, which will be the interval for holding constant safety stock and will be based on the highest amount of safety stock required for the 3 weeks in an interval. The smoothing happens by starting at the peak interval of safety stock requirement and reducing or increasing the safety stock as needed in the next interval before and after to be within the maximum percentage variation specified.

The following image shows an example of how raw safety stock is smoothed out over a 9-week duration (3 intervals of 3 weeks each). First, within each interval, safety stock is leveled up to the highest within-interval value. Then, the maximum percentage variation limits are imposed across intervals as necessary. This process continues until the safety stock in all intervals in the plan are adjusted.

Example of Safety Stock Smoothing

Safety stock rounding is done intelligently to minimize compounded rounding effect and also to handle the case of intermittent demands. If the Rounding Control item attribute is set to Yes, then the following method is used to round the safety stock at various levels of the supply chain:

1. Round up the safety stock at the end-item level. Compute the difference between the rounded up safety stock value and the actual value.
2. Subtract the difference from the safety stock at the next level in the supply chain. Round up the resulting safety stock and compute the difference, as stated in step 1.
3. The process is repeated all the way up the supply chain.

In traversing the supply chain, the logic ensures that the sum total of the safety stock across the echelons is equal to the rounded up integer value of the computed safety stock.

For example, in a supply chain of an end item A, the safety stock rounding at every level using this logic is shown in the following images:

Supply Chain Bill of Item A

Example of Safety Stock Rounding Calculation

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 🔐 Access Requirements

There are no additional security privileges needed to use this feature.

---
*Oracle Cloud Readiness · 26C · SCM · Sales and Operations Planning*