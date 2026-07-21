[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Improvements to Assign Load with Auto-Generated Load Number

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50168.htm)

Mobile Assign Load transaction now supports automatic Load Number generation, allowing warehouse users to assign loads without manually scanning or entering a Load Number. This simplifies the load assignment process, reduces user effort, and improves operational efficiency during outbound processing.

A new screen parameter: **auto-generate-load-number** is introduced with following values:

• Yes: WMS generates the load number after the user scans the order number based on the sequence counter.
• No/Blank (default): WMS retains the existing behaviour.

## ⚙️ Steps to Enable and Configure

1. Go to the Mobile Assign Load screen parameters.
2. Set **auto-generate-load-number** to Yes.
3. Keep the value as Blank or No to continue the existing manual load number entry flow.
4. WMS generates the load number after user scans the order number.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*