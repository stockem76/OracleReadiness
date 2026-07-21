[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Manufacturing](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/manufacturing.md)

# Add an Item Structure or Formula to an Existing Recipe

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/mfg26c/26C-mfg-wn-f49503.htm)

Manufacturing engineers may need to create recipes without having to start with the structure or formula, especially when the structure or formula is managed externally or still evolving. This provides the flexibility for prototyping, engineer-to-order, and formula optimization scenarios where the structure or formula isn't yet finalized.

This update lets you add a structure or formula name after a recipe is saved if a name wasn't initially specified. Here's how the feature works in the UI and with FBDI, ADFdi and REST:

• User Interface: 
  • Adding a formula name 
    • Ad hoc operation items and outputs are automatically deleted after a warning message.
• Operation items and outputs are automatically assigned based on the structure or formula suggested operation sequence.
• Adding a structure name 
    • Ad hoc operation ingredients are automatically deleted after a warning message.
• Ad hoc products are retained.
• Operation ingredients are automatically assigned based on the structure suggested operation sequence.
• File-Based Data Import (FBDI): 
  • Adding a formula name 
    • Ad hoc operation ingredients and products are automatically deleted, and a warning is captured in the output file.
• Automatic assignment of operation ingredients and products isn't performed.
• Adding a structure name 
    • Ad hoc operation ingredients are automatically deleted, and a warning is captured in the output file.
• Ad hoc products are retained.
• Automatic assignment of operation ingredients isn't performed.
• Using ADFdi and REST: 
  • Structure name or formula name can be added only if no ad hoc operation ingredients or products exist.
• If they exist, an error is captured.
• Automatic assignment of operation ingredients and products isn't performed.

Adding a Formula Name

Enabling the addition of a structure or formula name after a recipe is saved eliminates the need for creating a new recipe. This flexibility lets you define and adjust the recipe while the formula is being optimized and finalized, enhancing the efficiency of your product build process.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• This feature is available only with the Redwood experience, which can be enabled using the profile option, **Redwood Work Definitions Enabled**.
• This feature is also applicable to discrete manufacturing, flow manufacturing work definitions. Refer to the 26C feature: Add an Item Structure or Formula to an Existing Work Definition.
• Adding a structure or formula name is allowed only if a structure or formula name isn't initially specified during recipe creation.
• This feature isn't applicable if Electronic Records and Electronic Signatures (ERES) are enabled for manufacturing recipes. You must create a new recipe to add a structure or formula name.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Manage Work Definitions (WIS_MANAGE_WORK_DEFINITIONS_PRIV)
• View Work Definitions (WIS_VIEW_WORK_DEFINITIONS_PRIV)
• Get Work Definitions by Service (WIS_GET_WORK_DEFINITIONS_SERVICE_PRIV)
• Manage Work Definitions by Service (WIS_MANAGE_WORK_DEFINITIONS_SERVICE_PRIV)

These privileges were available prior to this update.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: Refer to the Using Manufacturing guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Refer to the Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Manufacturing*