[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Consumption Allowance Revenue Recognition

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f47279.htm)

Use enhanced revenue recognition support for allowance-based usage rating models in Oracle Subscription Management. You can now manage revenue recognition for subscriptions where customers purchase a defined quantity-based allowance, consume against that allowance during a balance period, purchase top-ups, roll over unused allowance, and incur overage when usage exceeds the available allowance- all this in accordance with ASC606/IFRS15.

Recurring charges that grant the base allowance are recognized over time. Top-up charges are recognized as the top-up allowance is consumed or expires. Overage usage is treated as additional revenue for the same service and is linked to the revenue contract for the allowance-granting performance obligation, instead of creating a separate performance obligation.

This enhancement helps you support usage-based subscription offerings while aligning revenue recognition with the way allowance, top-up, rollover, and overage usage are consumed. It reduces manual handling of allowance-based revenue scenarios and provides a consistent process for sending allowance consumption, top-up satisfaction, and overage revenue details to Oracle Revenue Management.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• Use this feature for **newly created balance registers**. Existing subscriptions continue to use the current usage revenue model.
• Use a **recurring charge** to grant the base allowance. A recurring base allowance charge is recognized over time using period-based satisfaction.
• Use a **one-time charge** for top-ups. Only a one-time charge can be marked as a top-up charge, and top-up charges are quantity satisfied.
• Top-up revenue is recognized when the top-up allowance is **consumed or expires**. If unused top-up allowance remains at the end of the balance period, a satisfaction event is sent for the unused quantity.
• Overage usage is **not created as a separate performance obligation**. It is treated as additional revenue for the same service and sent to RMCS with attributes that add it to the appropriate revenue contract.
• Overage is linked to the revenue contract for the allowance-granting performance obligation that the usage was last drawn from. This is especially important when multiple allowance grants or top-ups are available.
• Rollover affects allowance availability, but it does **not** add revenue contract impact. Rollover duration is not sent to RMCS.
• Amount-based allowances and multiple allowances converted into a single revenue subline are not part of the new model and continue with the existing revenue contract behavior.
• Keep all products in a balance register in the **same currency and business unit**.
• If a consuming product starts before the allowance-granting product or top-up product, usage for the period before the allowance is available is recognized using the existing standalone usage revenue contract model.
• If allowance quantity is manually updated after activation, the related revenue line may need to be synchronized through a new version line so RMCS reflects the revised allowance quantity.
• For subscription close actions, recurring allowance grants follow the normal recurring revenue close behavior, while one-time allowance grants may require reversal of the granted quantity through a negative satisfaction event.
• Usage corrections and re-rating are supported, but overage revenue remains tied to the original related performance obligation once reported, so downstream RMCS adjustments stay consistent.

## How the Feature Works

This feature supports revenue recognition for quantity-based allowance usage models in Oracle Subscription Management. A recurring charge can grant a base allowance that is recognized over time, while a one-time top-up charge can increase the available allowance and is recognized as the top-up allowance is consumed or expires. Usage is matched against the available base allowance, top-up allowance, and then overage. Any usage that exceeds the available allowance is treated as overage revenue and linked to the revenue contract for the performance obligation from which the usage was last drawn. The consumption is first applied to the base allowance, then to top-up or additional base allowance, and finally to overage for immediate recognition.

The feature supports allowance usage across subscription products and subscriptions through a shared balance register. This lets allowances granted by different products contribute to a common allowance pool, while consuming products draw down from that pool. The supported scenarios are allowances with one or more subscriptions, one or more products, recurring allowance grants, top-up allowance grants, rollover periods, and overage creation in RMCS. This is across lifecycle events such as close, amendment, proration, allowance adjustments, usage corrections, and re-rating.

## Prerequisites

Before using this feature, customers must set up an allowance-based usage model with a balance register and quantity-based allowance grants. For the new revenue behavior to apply, the balance register must be newly created; existing subscriptions using the allowance-based model continue to recognize revenue using the current usage model where revenue contracts are created upon billing.

The subscription products in a single balance register should use the same currency and business unit. Avoid mixed-currency or mixed-business-unit balance register scenarios.

Business benefits include:

• **Improves ASC 606 alignment for usage-based subscriptions**

   Supports revenue recognition for allowance-based consumption models where customers buy a committed allowance, consume against it, and may incur top-up or overage charges.
• **Connects overage revenue to the right performance obligation**

   Overage usage is linked back to the revenue contract for the allowance-granting performance obligation, helping revenue teams recognize usage revenue in the appropriate contract context.
• **Supports flexible monetization models**

   Enables subscription offerings that include base allowances, top-ups, rollovers, and overage usage, giving customers more ways to package and sell consumption-based services.
• **Reduces manual revenue accounting effort**

   Automates the handling of allowance consumption, top-up satisfaction, and overage revenue lines, reducing manual intervention and reconciliation between Subscription Management and RMCS.
• **Improves revenue accuracy for top-ups**

   Recognizes top-up revenue as the top-up allowance is consumed or expires, helping ensure revenue reflects actual customer usage.
• **Supports pooled allowance models**

   Allows allowances granted by different subscription products or subscriptions to be consumed from a shared balance register, supporting more complex enterprise subscription arrangements.
• **Preserves existing behavior for out-of-scope scenarios**

   Existing subscriptions and certain unsupported scenarios continue to use the current usage revenue model, reducing disruption during adoption.
• **Improves auditability and traceability**

   Captures usage, allowance, top-up, and overage details needed to trace how consumption was apportioned and how revenue was sent to RMCS.
• **Enables more accurate handling of subscription lifecycle events**

   Supports revenue behavior for amendments, closures, allowance updates, proration, corrections, and re-rating scenarios, helping keep revenue contracts aligned with subscription changes.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*