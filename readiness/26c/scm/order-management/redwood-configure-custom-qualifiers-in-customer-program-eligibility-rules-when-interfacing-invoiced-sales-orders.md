[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Order Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/order-management.md)

# Redwood: Configure Custom Qualifiers in Customer Program Eligibility Rules when Interfacing Invoiced Sales Orders

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/order26c/26C-order-mgmt-wn-f46541.htm)

Configure custom qualifiers for customer program eligibility rules in customer rebate and customer volume programs when interfacing invoiced sales order transactions directly to Channel Revenue Management. The custom qualifiers are based on AR invoice header and line descriptive flexfield values.

Realize these benefits:

• Apply rebate eligibility rules that match customer-specific agreements.
• Support more complex promotional or volume-based programs without custom integrations.
• Use existing configuration for mapping the sales order extensible attributes with the AR Invoice descriptive flexfields.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Order Management*

1. If you have already implemented Customer Programs, then you don't need to do anything to enable this feature.
2. If you haven’t implemented Customer Channel Programs, then refer to the **Roadmap for Setting up Customer Channel Programs** chapter in the **Implementing Channel Revenue Management** guide.
3. Refer to the **How to Set Up Custom Qualifiers Based on Sales Invoice Header Descriptive Flexfields** and **Set Up Custom Qualifiers Based on Sales Invoice Line Descriptive Flexfields**chapters in the implementation guide, **Implementing Channel Revenue Management**.
4. Refer to Use Extensible Flexfields to Integrate Order Management with Oracle Applications

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• **Manage Customer Programs** (CJM_MANAGE_CUSTOMER_PROGRAMS_PRIV)
• **View Only Activity** (ZMM_VIEW_ONLY_ACTIVITY_PRIV)

These privileges were available prior to this update.

## 📚 Key Resources

• Watch Introduction to Customer Channel Management.
• For more information on Channel Revenue Management, refer to the **Oracle Cloud Readiness** content for **Order Management.**
• For more information on the Channel Revenue Management Integration with Receivables, refer to the **Oracle Cloud Readiness**content for **Financials.**
• Oracle SCM Cloud: Using Oracle Channel Revenue Management Cloud, available on the Oracle Help Center.
• Oracle SCM Cloud: Implementing Oracle Channel Revenue Management Cloud, available on the Oracle Help Center.
• Oracle SCM Cloud: REST API for Oracle SCM Cloud, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Order Management*