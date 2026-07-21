[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Global Trade Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/global-trade-management.md)

# Enhancements to License Management

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/gtm26c/26C-gtm-wn-f49597.htm)

This feature enhances license management to better support scenarios that use both license reservation and license assignment. With these enhancements, you can:

• Set the **Allow Supplement from Balance** flag to permit assignment of license quantities or values that exceed previously reserved amounts.
• Use the **Adjust License** action to update the reserved balance.

**Set Allow Supplement from Balance Flag**

License management enables you to reserve license quantities and values upon receipt of a sales order to help ensure compliance. However, when goods are shipped, the actual quantity or value assigned may exceed the reserved amount. By enabling the **Allow Supplement from Balance** flag on the license header, GTM can automatically supplement any shortfall by drawing the additional required quantity or value from the license line at shipment time, while continuing to use the reserved quantity or value from the existing sales order.

License - Allow Supplement from Balance Field

**Adjust License Action for Reserved Balance**

In addition to license assignments, the **Adjust License** action now supports license reservations. A new field, **Adjust Type**, is available on the action and allows you to specify whether you are adjusting a **RESERVATION** or an **ASSIGNMENT**. Selecting **RESERVATION** adjusts the reserved license balance, while selecting **ASSIGNMENT** adjusts the assigned license balance.

Adjust Balance Action on License

**Business Benefit:**These enhancements provide greater flexibility in managing licenses by allowing assignments to continue even when reserved quantities are exceeded. They also improve operational efficiency and accuracy by enabling administrators to easily adjust reserved balances as business needs change.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

The **Allow Supplement from Balance** flag works similarly to the optional feature **Assign Additional Value from License** introduced in 26A. However, by enabling the flag directly on the license, you can control and apply this capability at a more granular level.

---
*Oracle Cloud Readiness · 26C · SCM · Global Trade Management*