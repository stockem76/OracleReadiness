[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Manufacturing](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/manufacturing.md)

# Assign and Sync Global Work Definitions Using FBDI

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/mfg26c/26C-mfg-wn-f44507.htm)

In the previous update, you could create a global work definition in an item master organization and assign it to child organizations enabled as manufacturing plants using the Redwood page for Work Definition. With this update, you can now use File-Based Data Import (FBDI) to assign and synchronize a global work definition with all child organizations. A new column Replicate Global Work Definition is now included in the FBDI templates for discrete manufacturing and process manufacturing. This column is applicable only for the item master organization. Specifying Yes when creating a new work definition in an item master organization creates the work definition as a global work definition and automatically assigns it to all child organizations. When updates are made to the global work definition, changes are synchronized to all child organizations regardless of the value specified for Replicate Global Work Definition.

Creating and updating a global work definition using FBDI works as follows:

• Create 
  • Created in the item master organization if validations pass.
• Copied only to child organizations where validations pass.
• Update 
  • Updated in the item master organization if validations pass.
• Synced to child organizations only if validations pass in all child organizations.
• Add or Delete Version 
  • Completed only if validations pass in the item master and all child organizations.
• Deactivate or Reactivate 
  • Completed only if validations pass in the item master and all child organizations.

**File-Based Data Import (FBDI) Changes:**

The FBDI discrete work definition template, WorkDefinitionTemplate.xlsm, and process work definition template, ProcessWorkDefinitionTemplate.xlsm, are enhanced to enable the assignment and synchronization of global work definitions with child organizations. A new column Replicate Global Work Definition has been added to the Work Definition Headers worksheet. Use the latest template after upgrade to 26C.

A global work definition lets you centrally create and manage a work definition in the item master organization. This facilitates a streamlined change management process and reduces the time spent in managing work definitions that are common across organizations. Global work definitions help maintain work definition accuracy as changes are controlled centrally.

## ⚙️ Steps to Enable and Configure

If you want to use the Assign and Sync Global Work Definitions Using FBDI, then you must opt in to another feature Redwood: Manage Global Work Definitions in an Item Master Organization. If you’ve already opted in to this other feature, then you don’t have to opt in again.

## 💡 Tips and Considerations

• This feature is applicable to Discrete Manufacturing, Flow Manufacturing, and Process Manufacturing.
• As a best practice, set up a single item master organization and enable it as a manufacturing plant.
• The following building blocks that make up a global work definition in an item master organization must exist in the child organization:  
  • Items
• A common item structure or formula. Formulas are applicable to process manufacturing.
• Work definition name
• Production line code - Applicable to flow and discrete manufacturing
• Standard operation code
• Work center code
• Resource code
• A global work definition can't be created in an item master org if electronic signatures are enabled for work definitions in the organization.
• A global work definition can't be assigned to a child organization if electronic signatures are enabled for work definitions in the organization.
• A global work definition can't be an automatic work definition.
• Assigning a global work definition using ADFdi and REST APIs is currently not supported.
• You can continue to create a work definition directly in a child organization with no change in behavior.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Load File to Interface (FUN_FSCM_FILE_TO_INTERFACE_PRIV)
• Load Interface File for Import (FUN_FSCM_LOAD_INTERFACES_PRIV)
• Manage File Import and Export (FND_MANAGE_FILE_IMPORT_AND_EXPORT_PRIV)
• Transfer File (FUN_FSCM_TRANSFER_FILE_PRIV)
• Import Work Definitions (WIS_IMPORT_WORK_DEFINITIONS_PRIV)

These privileges were available prior to this update.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: Refer to the Using Manufacturing guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Refer to the Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Manufacturing*