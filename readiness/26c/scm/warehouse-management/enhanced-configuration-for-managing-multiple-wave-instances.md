[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Enhanced Configuration for Managing Multiple Wave Instances

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f49717.htm)

The **ONLY_ONE_WAVE_PER_FACCO** company parameter now supports additional values that define how strictly WMS controls concurrent wave activity. You can choose whether to allow waves to run together by template, restrict waves by type, or enforce a single wave-related process at a time.

This enhancement gives operations teams more control over simultaneous wave processing, helping balance high-frequency wave execution with safeguards that prevent conflicting wave runs.

**ONLY_ONE_WAVE_PER_FACCO Values**

**NOTE:**Run Wave and Undo Wave now use consistent locking behavior so the configured concurrency rule is applied across both actions.

## ⚙️ Steps to Enable and Configure

1. Review the **ONLY_ONE_WAVE_PER_FACCO** company parameter and set the value that matches your operational flow: **one-per-wave-template, one-per-wave-type, or enforce-single-wave.**
2. Set the **ONLY_ONE_WAVE_PER_FACCO** company parameter to No for **one-per-wave-template**.
3. Set the **ONLY_ONE_WAVE_PER_FACCO** company parameter to Yes for **one-per-wave-type**.

**NOTE:** Customers choosing one-per-wave-template or one-per-wave-type should evaluate whether different wave templates or wave types may still select overlapping orders or inventory.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*