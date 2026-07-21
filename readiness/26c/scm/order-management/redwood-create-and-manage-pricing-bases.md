[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Order Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/order-management.md)

# Redwood: Create and Manage Pricing Bases

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/order26c/26C-order-mgmt-wn-f46575.htm)

Use the redesigned Redwood Pricing Bases page to create and manage pricing bases with the same underlying functionality as the existing ADF page.

The redesign preserves the existing pricing basis functionality, so you continue to work with the same pricing basis concepts and setup behaviour as before.

Get these benefits:

• Search for pricing bases by name or description from a single search box.
• Refine the results with filters for Usage, Accumulation Unit, Price Element, and Active.
• Open the create side panel directly from the Redwood page and enter the pricing basis details there.
• Create a pricing basis without leaving the main Redwood experience.
• Use row actions to view, duplicate, edit, or delete pricing bases where deletion is allowed.

You can manage pricing bases in a more modern interface and find, review, and maintain bases more efficiently through streamlined search, filters, and direct row actions.

Oracle Pricing now provides a redesigned Redwood Pricing Bases page for creating and managing pricing bases.

The page introduces a streamlined search experience with a single search box for name or description, filter chips for Usage, Accumulation Unit, Price Element, and Active, and direct actions to create, view, duplicate, edit, or delete pricing bases.

Start on the redesigned Pricing Bases page, where you can search for existing bases, refine the results with filters, or click **Create**to begin a new pricing basis:

Create New Price Basis

When you click **Create**, Redwood opens a side panel where you can enter the basis name, description, usage, price element, active status, and charge criteria for included or excluded charges:

New Pricing Basis Page Showing All Required Fields

After you enter the required values and charge criteria, click **Create**to add the pricing basis without leaving the Redwood page:

Pricing Bases Page Showing the Newly Created Pricing Basis

## ⚙️ Steps to Enable and Configure

You must enable the ORA_QP_PRICING_BASES_REDWOOD_ENABLED

   (Redwood Page for Pricing Bases Enabled)

Follow these steps to enable this feature:

1. In the Setup and Maintenance work area, select the **Tasks**panel. Select **Search**, and then search for and select the **Manage Administrator Profile Values** task.
2. On the Manage Administrator Profile Values page, search for and select the **ORA_QP_PRICING_BASES_REDWOOD_ENABLED** profile option code.
3. In the Profile Values section, set the **Site**level to Yes.  
  • Yes = enables the feature
• No = disables the feature
4. Click **Save and Close**. Changes in the profile value will affect users the next time they sign in.

## 💡 Tips and Considerations

• The redesigned page doesn’t change the underlying pricing basis functionality.
• Use predefined pricing bases when possible, to reduce maintenance.
• Predefined pricing bases can't be deleted.
• Use the search box and filter chips to quickly narrow the list of pricing bases before you create or update one.
• Tier basis setup can include or exclude charges and can reference charge details such as price type, charge type, charge subtype, and frequency.
• Review the required values and charge criteria in the create side panel before you click **Create**.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Manage Pricing Bases (QP_MANAGE_PRICING_BASES_PRIV)
• View Pricing Bases (QP_VIEW_PRICING_BASES_PRIV)

These privileges were available before this update.

## 📚 Key Resources

• Administering Pricing
• Manage Pricing Bases

---
*Oracle Cloud Readiness · 26C · SCM · Order Management*