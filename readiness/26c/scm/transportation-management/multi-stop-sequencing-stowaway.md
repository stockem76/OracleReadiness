[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# Multi-stop Sequencing Stowaway

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f49730.htm)

In Multi-stop, it is possible that a shipment may load an order early in the tour and retain it even though the truck may return to the destination stop one time before it is actually delivered.  This enhancement revises the sequence logic to avoid that. While it sounds like this should be always active, the necessity to avoid regressing issues requires a new parameter.

Notice the difference in the Logic Configuration.  It is recommended that this be set to true when using the MSMS logic.  It is also advisable to use this with MS.

Multi-stop Logic Configuration

Scenario with bad sequence.

Bad Sequence

Bad Running Manifest

Good Sequence

Good Running Manifest

**Business Benefit:**The business benefit is very obvious.  More efficient utilization.

## ⚙️ Steps to Enable and Configure

You will need to set the Parameter ENFORCE CLEAN HANDOFF CHECK IN SEQUENCING to TRUE to take advantage of this new logic.

## 💡 Tips and Considerations

This is a change in the sequencing logic so it is a parameter enabled to avoid any regression issues.

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*