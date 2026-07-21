[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Global Trade Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/global-trade-management.md)

# Asynchronous Support for Restricted Party Screening

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/gtm26c/26C-gtm-wn-f46360.htm)

This feature introduces asynchronous processing for the Customs Actions Restricted Party Screening REST APIs by supporting the "Prefer: respond-async" request header. With this enhancement, you can submit restricted party screening requests for asynchronous execution.

**Business Benefit:**By allowing requests to be executed asynchronously, it improves system scalability and responsiveness, especially for high-volume screening operations. Users can submit screening requests without waiting for immediate completion, reducing latency impacts on client applications and enabling more efficient handling of large or complex workloads.

## ⚙️ Steps to Enable and Configure

You can utilize the new asynchronous option by inclduing the "Prefer"  - "respond-async" request header. By default, requests are processed synchronously.

---
*Oracle Cloud Readiness · 26C · SCM · Global Trade Management*