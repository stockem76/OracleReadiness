[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Sales and Operations Planning](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/sales-and-operations-planning.md)

# Optimize Inventory Levels Across Multiple Echelons

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/sop26c/26C-sales-ops-wn-f45784.htm)

You can now optimize stock levels at each node and improve inventory placement efficiency using postponement and risk pooling heuristics to lower buffer inventory. This also increases planning accuracy by supporting demand and lead-time variabilities.

With this update, you can optimize inventory levels across multiple echelons to meet demand on time while minimizing total inventory investment. The optimization process calculates time-phased safety stocks based on demand uncertainty, service levels, and cumulative lead times, enforcing user-specified safety stocks before applying item and organization service levels. It also applies postponement heuristics to allocate safety stocks down the bill of materials and sourcing tree, considering node lead times, while risk pooling further reduces buffer inventory in units and value.

Inventory optimization planning considers the following key factors in planning safety stock levels:

• **Target service level** **percentages** **(and demand fulfillment lead times)**: These can be specified at a plan level and can also be specified for individual item segments.
• **Demand variability**: This is represented by the forecast error specified in plan options. For regular, nonintermittent demand, it’s based on mean absolute deviation (MAD) or mean absolute percentage error (MAPE). For intermittent demand, it uses the average interarrival time specified in the plan options.
• **Lead time variabilities**: These can be expressed either as a coefficient of variation or absolute days. The lead time variabilities can be for any of the following:
• Manufacturing lead time variability (for each item-location)
• In-transit lead time variability (for each item-location and source-organization combination)
• Purchasing lead time variability (for each item and supplier-site combination)

**Postponement**

Inventory optimization planning applies postponement heuristics to postpone the overall end item safety stocks based on the overall lead times and costs to upstream facilities in a multiechelon supply chain and to components for manufactured items. While doing so, it evaluates possible alternate sources, work definitions, and substitute components to achieve the target service level and to minimize overall inventory costs.

Postponement Across Echelons

**Risk Pooling**

Wherever feasible, inventory optimization planning leverages risk pooling at shared (common) nodes across a multiechelon supply chain network. Such pooling of risk at common item-locations in the supply chain reduces the impact of independent random variations in downstream nodes and potentially reduces the overall safety stock inventory.

Risk Pooling Across Echelons

Similarly, risk pooling happens not just for the same item across locations (holding an inventory buffer of an item at a common upstream location that feeds the item to multiple downstream locations), but also across bills of material that share common components. If a component is shared across many finished goods, its prescribed safety stock level will be lower than if the component is used in only one or a few finished goods.

**Scope**

Inventory optimization planning uses item segments to identify the scope of the plan. Item segments are defined using the Segment Groups and Criteria task. After the segments are defined, you can specify the segments to be planned in the plan options. Segments must be defined only at product and organization dimensions.

The scope of an inventory optimization plan is defined by the end items from the demand schedule, which are also part of the segments specified in the plan options. So, as shown in the following example, only “FG A” will be included in the plan because it’s common among the demand schedule and the included item segments.

Using Segments to Define the Scope

Similarly, for components and their upstream items, only those that are part of the segments included in the scope of the plan are considered. Any items that are in that chain but not part of the segments will be included to complete the supply chain. So, in the following example, “Subassembly C” will be included even though it’s not part of the segments.

Scope of Planned Items

An inventory optimization plan includes all items with their Planning Method attribute set to MRP, MPS, MPP, or Replenishment Planning.

For the end items in the scope of the plan, inventory optimization planning uses forecast demand and any manual demand from a simulation set. It doesn’t use sales orders. And it also doesn’t use any existing supplies but instead generates net new planned orders as needed to meet the safety stock requirement. Inventory optimization also doesn’t use any order modifiers while creating the new planned orders.

**Forecast Spreading**

Inventory optimization planning spreads the forecast to the plan buckets evenly, which reduces any unnecessary safety stock spikes. As an example, if the forecast for a period is 30 and the plan is run in weekly buckets, then the safety stock is spread as shown in the following table. This example assumes the rounding control is on for this item and therefore the forecasts will be rounded up.

Example of Forecast Spreading

**Run Plan**

You can run an inventory optimization plan using the Run Plan task. An inventory optimization plan always runs by refreshing the current data from the collected data related to the master data and current forecasts from the demand schedule.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains this privilege can access this feature:

• Run Plan with Snapshot (MSC_RUN_PLAN_WITH_SNAPSHOT)

This privilege was available prior to this update. The Inventory Optimization Planner job role already includes this privilege.

---
*Oracle Cloud Readiness · 26C · SCM · Sales and Operations Planning*