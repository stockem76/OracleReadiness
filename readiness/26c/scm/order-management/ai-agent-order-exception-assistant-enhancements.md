[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Order Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/order-management.md)

# AI Agent: Order Exception Assistant Enhancements

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/order26c/26C-order-mgmt-wn-f49710.htm)

You can now resolve selected fulfillment, functional, and technical order exceptions directly from the Oracle Exception Assistant.  You can also review affected orders and lines, understand why processing stopped, and take guided actions such as processing pending fulfillment responses, canceling eligible tasks, recovering orders, checking availability, or continuing orchestration.

**Get these benefits**

•    Resolve common order-processing interruptions without manually tracing fulfillment responses, orchestration state, availability, reservation quantity, or technical recovery steps across multiple pages.

  •     Use a guided path to process pending responses, recover eligible errors, continue orchestration, and make informed line-level decisions. 

  •    Reduce exception investigation time, improves order progression, and lowers support effort for orders that are waiting on a response, recovery action, or user decision.

## ⚙️ Steps to Enable and Configure

This feature is available as part of Order Exception Assistant. No separate opt-in is required.

Users can access the assistant from the Order Management dashboard, order context, or exception context, depending on the order state and exception type.

## 💡 Tips and Considerations

• The assistant processes callback exceptions only when the related callback or response data exists and has not yet been processed.
• For GTM and OTM, the assistant explains the two-step flow: acknowledge the task, then wait for the response. The line does not complete until both steps finish.
• For functional exceptions, the available actions depend on the response returned by availability, reservation, or on-hand checks.
• For technical exceptions, user approval or the required recovery privilege may be needed before the assistant can force edit, create an order revision, run Recover Errors, or continue orchestration.

## 🔐 Access Requirements

Get access instructions here: AI Agent: Order Exception Assistant.

## 📚 Key Resources

• AI Agent: Order Exception Assistant

---
*Oracle Cloud Readiness · 26C · SCM · Order Management*