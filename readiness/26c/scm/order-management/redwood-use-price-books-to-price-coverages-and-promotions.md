[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Order Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/order-management.md)

# Redwood: Use Price Books to Price Coverages and Promotions

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/order26c/26C-order-mgmt-wn-f46584.htm)

You can now use a price book to price a coverage or promotion in your quote or sales order.

Realize these benefits:

• Flat rate coverage pricing is based on lookup to price book.
• Promotions that do not rely on order data are priced through price book data.
• Volume pricing through line and document-based tiers is now fully supported through price books.
• Discounts placed on models are also supported through price books.

You can continue to use price books for runtime pricing just as you have been doing. The enhancements provided by this update are available automatically.  If you set up promotions that don’t rely on order data (no eligibility or additional buy items rules), or if you have coverages that aren’t dependent on the covered item price, then they are now included in the price book. Volume pricing through tier setup is also completely supported now.

The following screenshot demonstrates pricing a sales order using a customer-specific price book that contains a promotion called Spring Savings. The benefit for this promotion includes a 10% discount for 2 item categories, Computers and Accessories.

Pricing Sales Order with Price Book Promotion

The following screen shot shows the detail for the order line of the Custom Laptop, which is a member of the item category, Computers. You can see the message documenting the promotion discount and the amount of the discount in the charge breakdown.

Sales Order Detail - Promotion

The following screen shot shows the pricing behavior for an item that’s not a member of the item categories participating in the promotion benefit. No discount is taken.

Sales Order Detail - No Promotion

## ⚙️ Steps to Enable and Configure

If you want to use this feature, then you must opt in to these features: Redwood: Use Price Books to Price Sales Orders and Redwood: Create Price Books to Price Sales Orders. If you’ve already opted in to these features, then you don’t have to opt in again.

## 💡 Tips and Considerations

• You must generate the price book before you can use it in Order Management. See Redwood: Create Price Books to Price Sales Orders.
• You don't need to make any changes in Oracle Order Management to use this feature. If you opt in and generate the price book, then Pricing uses that book if it's available. Otherwise, Pricing uses the item's standard pricing.
• You can create and use a price book only on the redesigned Pricing and Order Management pages.

You can't include these items or pricing on a price book in update 26C:

• Configured item with discount pricing for pricing rollups. Discounts are taken for components.
• Coverage pricing based on item prices. For communication purposes, placeholder values are shown in the price book, but they aren’t used for pricing at runtime. Pricing is carried out by the runtime pricing engine instead.
• Promotions that contain eligibility rules or additional buy item rules.

If your price list has one of them, then the price book doesn’t include it.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

  PRICING:

• Manage Pricing Rules (QP_MANAGE_PRICING_RULES)
• View Price Lists (QP_VIEW_PRICE_LISTS_PRIV)
• Manage Price Lists (QP_MANAGE_PRICE_LISTS_PRIV)
• Manage In-Progress Price Lists (QP_MANAGE_IN_PROGRESS_PRICE_LISTS_PRIV)
• Generate Price Book (QP_GENERATE_PRICE_BOOK_PRIV)  Generate a price book from user-selected parameters.
• View Price Books (QP_VIEW_PRICE_BOOKS_PRIV)  Allows viewing of price books.
• Manage Price Books (QP_MANAGE_PRICE_BOOKS_PRIV)  Allows creation, update, deletion, and viewing of price books.
• Delete Price Books (QP_DELETE_PRICE_BOOKS_PRIV)  Allows deletion of price books.
• Publish Price Books (QP_PUBLISH_PRICE_BOOK_PRIV)  Publish a price book that was previously generated.

These privileges were available before this update.

## 📚 Key Resources

• Administering Pricing
• Manage Price Lists

---
*Oracle Cloud Readiness · 26C · SCM · Order Management*