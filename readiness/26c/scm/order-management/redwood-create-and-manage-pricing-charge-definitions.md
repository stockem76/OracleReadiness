[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Order Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/order-management.md)

# Redwood: Create and Manage Pricing Charge Definitions

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/order26c/26C-order-mgmt-wn-f46572.htm)

Use the redesigned Redwood Pricing Charge Definitions page to create and manage charge definitions with the same underlying functionality as the existing ADF page.

The redesign preserves the existing pricing charge definition functionality, so you continue to work with the same charge definition concepts and setup attributes as before.

Get these benefits:

• Search for charge definitions by code, name, or description from a single search box.
• Refine the results with filters for Applies To, Price Type, Charge Type, Charge Subtype, Active, and Setup Enabled.
• Open the **Create**side panel directly from the Redwood page and enter the charge definition details there.
• Create a charge definition without leaving the main Redwood experience.
• Use row actions to view, edit, or delete an existing charge definition.

You can manage pricing charge definitions in a more modern interface and find, review, and maintain definitions more efficiently through streamlined search, filters, and direct row actions.

Oracle Pricing now provides a redesigned Redwood Pricing Charge Definitions page for creating and managing charge definitions.

The page introduces a search experience with a single search box for code, name, or description, filter chips for key attributes, and direct actions to create, view, edit, or delete charge definitions.

Start on the redesigned **Pricing Charge Definitions** page, where you can search for existing definitions, refine the results with filters, or select **Create**to begin a new definition:

Create New Pricing Charge Definition

When you click **Create Charge Definition**, Redwood opens a side panel where you can enter the charge definition details, including code, name, description, applies to, price type, charge type, charge subtype, UOM classes, and related setup options:

New Charge Definition Page Showing All Required Fields

After you enter the required values, click **Create**to add the charge definition without leaving the Redwood page:

Charge Definitions Page with Newly Created Charge Definition

## ⚙️ Steps to Enable and Configure

You must enable the ORA_QP_PRICING_CHARGE_DEFINITIONS_REDWOOD_ENABLED (Redwood Page for Pricing Charge Definitions Enabled)

Follow these steps to enable this feature:

1. In the Setup and Maintenance work area, select the **Tasks**panel. Select **Search**, and then search for and select the**Manage Administrator Profile Values** task.
2. On the Manage Administrator Profile Values page, search for and select the **ORA_QP_PRICING_CHARGE_DEFINITIONS_REDWOOD_ENABLED** profile option code.
3. In the Profile Values section, set the **Site**level to Yes.  
  • Yes = enables the feature
• No = disables the feature
4. Click **Save and Close**. Changes in the profile value will affect users the next time they sign in.

## 💡 Tips and Considerations

• The redesigned page doesn’t change the underlying pricing charge definition functionality.
• Use predefined pricing charge definitions, when possible, to reduce maintenance.
• Use the search box and filter chips to quickly narrow the list of charge definitions before you create or update one.
• Review the required fields in the create side panel before you click **Create**.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Manage Pricing Charge Definitions (QP_MANAGE_PRICING_CHARGE_DEFINITIONS_PRIV)
• View Pricing Charge Definitions (QP_VIEW_PRICING_CHARGE_DEFINITIONS_PRIV)

These privileges were available before this update.

## 📚 Key Resources

• Administering Pricing
• Manage Pricing Charge Definitions

---
*Oracle Cloud Readiness · 26C · SCM · Order Management*