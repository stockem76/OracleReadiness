[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Supply Planning](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/supply-planning.md)

# Consider Item Lead Time as an Optional Constraint

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/scp26c/26C-sc-planning-wn-f45789.htm)

You can now specify whether the item lead times should be considered when calculating the production schedule and simulate schedule results based on that. Previously, the lead time was always enforced for consumers of any item’s shortage quantity.

A new schedule option is added that allows specifying whether the item lead times need to be ignored or considered when addressing inventory shortages during schedule calculation. Work order operations that consume such an item and are pegged to the shortage quantity are impacted.

Setting New Advanced Schedule Option

If **Ignore item lead times** setting isn't enabled, then dependent work order operations respect the lead times and are pushed out to schedule horizon start plus the component item's lead time. In the following example, the selected work order has a need-by date of January 7 but is pushed out to January 14 due to the item lead time consideration. This has been the default behavior until now and couldn’t be changed.

Respecting Item Lead Times for Shortages

For buy items, Production Scheduling uses preprocessing lead time plus procure lead time plus post-processing lead time from the item master. For make items the cumulative lead time is used, that corresponds to the total lead time of the assembly plus the largest cumulative lead time of its components. Consequently, if a manufactured sub-assembly has a shortage, any consuming operation is pushed out by the subassembly’s cumulative lead time. This happens even if the required materials to manufacture this subassembly were available and the manufacturing of the subassembly would only take 1 day. For example, assume such cumulative lead time for the subassembly to be 7 days. Even if all the materials to manufacture the subassembly were available and the subassembly’s processing time was only 1 day, then the downstream consumer is pushed out 7 days, which is too pessimistic, as you could produce that subassembly in just 1 day.

If Ignore item lead times setting is enabled, work order operations that depend on a component's shortage quantity can be scheduled as early as the internal data horizon start, effectively ignoring the material lead time constraint. In the given example, the selected work order with due date of January 7 is now scheduled that day, despite being pegged to an item shortage that is resolved only on January 14 based on having a 7-day lead time.

Ignoring Item Lead Time for Shortages

This way you can simulate the schedule outcome based on resource capacity and availability constraints.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Supply Chain Planning*

## 💡 Tips and Considerations

If you want to use the Consider Item Lead Time as an Optional Constraint feature, then you must opt in to its parent feature, Oracle Production Scheduling. If you’ve already opted into this parent feature, then you don’t have to opt in again.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains this privilege can access this feature:

Edit Production Schedule (MSC_EDIT_PRODUCTION_SCHEDULE_PRIV)

This privilege was available prior to this update.

---
*Oracle Cloud Readiness · 26C · SCM · Supply Planning*