[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# Redwood: Manage the Default Classification Group Using a Redwood Page

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f46489.htm)

You can view, search for, create, edit, and delete classifications for the default classification group. When setting up PAR and min-max planning for Oracle Inventory Management, create classifications to categorize items. You associate categories with similar item attributes with a classification. Categorizing items with similar attributes enables you to specify the policies for computing the PAR levels and min-max quantities efficiently.

For example, based on item cost, you can define classifications as high, medium, or low cost. You can then associate all the categories that contain high cost items to a classification called high cost.

You define all the classifications under the Default classification group, which acts as a placeholder for all the classifications. After creating classifications, you associate them with policy profiles at the organization and subinventory levels using the **Policy Profile Assignments** task.

Default Classification Group

This feature provides you with the ability to define default classification groups to group item categories into classifications for PAR and min-max replenishment.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 🔐 Access Requirements

To set up this feature, you'll need a configured job role that contains this existing privilege:

• Manage Min-Max Planning Policies (INV_MANAGE_MIN_MAX_PLANNING_POLICIES)

This privilege was available prior to this update.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: Using Inventory Management guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Security Reference for Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*