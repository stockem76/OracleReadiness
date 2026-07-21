[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Product Lifecycle Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/product-lifecycle-management.md)

# Redwood: Create Work Definition Automatically

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/plm26c/26C-plm-wn-f46463.htm)

A new **Create Automatic Work Definition**action on the structure now generates the work definition directly from an item’s primary structure when the eligibility criteria are met.

Here’s the eligibility criteria, including the fields and corresponding values:

Eligibility Criteria to Create Automatic Work Definition

Criteria 1 | Criteria 2
Organization is a manufacturing plant = Enabled Structure Type = is an approved item Structure Item Type = Standard Structure Name = Primary | Organization is a manufacturing plant = Enabled Structure Type = is an approved item Structure Item Type =Model Structure Name = Primary Assemble to Order = Yes

Validation rules are enforced before the action can be taken. If the required criteria aren’t met (for example, the structure isn’t approved, there’s a mismatch in structure type or item type, or Assemble to Order requirements aren’t satisfied), the action is **disabled**.

When the action is executed, the application generates the work definition. Additionally, the application validates prerequisites such as the existence of a valid work center and valid standard operation, prior to creating the definition.

Create Automatic Work Definition Action on a Structure

This feature benefits your business by the following:

• **Faster and more consistent work definition creation:** Automatically generating the work definition from the approved primary structure reduces manual setup effort and standardizes outputs. Thus helping teams bring items to production or ATO readiness more quickly.
• **Improved governance and fewer downstream errors:** Built-in eligibility checks such as approved structure, correct item type, ATO requirements, valid work center and operations, prevent invalid or incomplete work definitions from being created.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• You must save and commit updates before you select **Create Automatic Work Definition**.
• If the structure is created by copying an existing one, the work definition isn’t copied from the original structure. You must generate the definition.
• If the structure is created using **Create from Common**, the work definition won’t be common. You must generate the definition.
• The**Create Automatic Work Definition** action won't be allowed if there are pending changes in the item workbench. You can generate the work definition only if there aren’t any pending changes within the item transaction boundary.
• A valid manufacturing license is required for accessing work center and operations.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Manage Item Redwood Structures (EGP_MANAGE_REDWOOD_ITEM_STRUCTURE_PRIV)
• Manage Work Definitions by Service (WIS_MANAGE_WORK_DEFINITIONS_SERVICE_PRIV)

These privileges were available prior to this update.

## 📚 Key Resources

• Create Automatic Work Definitions for ATO Models in Manufacturing What's New 26B.
• Oracle Fusion Cloud SCM Using Product Development Guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM Using Product Master Data Management Guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Product Lifecycle Management*