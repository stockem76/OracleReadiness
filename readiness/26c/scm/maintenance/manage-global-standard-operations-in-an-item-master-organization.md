[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Maintenance](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/maintenance.md)

# Manage Global Standard Operations in an Item Master Organization

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/maint26c/26C-maintenance-wn-f44537.htm)

Manufacturers need a scalable way to standardize and maintain identical standard operations across multiple organizations to support multi-plant rollout, contract manufacturers, and global maintenance programs.

With this update, you can now create a global standard operation in an item master organization enabled as a manufacturing plant or maintenance organization and assign it to child organizations enabled as manufacturing plants or maintenance organizations. When you are in the item master organization, a new action Assign Global Standard Operation is available on the Standard Operations page.

You can selectively assign a global standard operation to chosen child organizations or to all child organizations. The assignment is processed by the Propagate Global Standard Operations scheduled process. The results and errors, if any, are captured in the output file of the scheduled process. You need to monitor the scheduled process, review the output file, and take appropriate actions to resolve the errors.

Assign Global Standard Operation Action

Assign a Global Standard Operation to Child Organizations

Global Standard Operation Scheduled for Assignment

If a global standard operation is successfully assigned, a replicated standard operation is created in the child organization. The replicated standard operation is read-only except for the indicator "Replicated". If you deselect the Replicated checkbox, the replicated standard operation is unlinked from the global standard operation and becomes an independent standard operation. Any subsequent changes to the global standard operation are no longer synced with the child organizations. If you unlink a standard operation for a child organization, you cannot link it again.

Replicated Standard Operation in a Child Organization

Updating and deleting a global standard operation is also processed by the Propagate Global Work Definitions scheduled process. If this action fails in a child organization, the change isn’t committed in the item master organization or any child organization. After correcting the errors, you need to perform the action again in the item master organization.

Centralizing standard operations management in the item master organization improves operational efficiency. It also maintains data integrity by automating synchronization of changes across manufacturing plants.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Manufacturing and Supply Chain Materials Management*  No Longer Optional From: *Update 27A*

## 💡 Tips and Considerations

• This feature is available only with the Redwood experience, which can be enabled using the profile option, **Redwood Standard Operations Enabled**.
• As a best practice, set up a single item master organization and enable it as a manufacturing plant or maintenance organization.
• The following building blocks that make up a global standard operation in an item master organization must exist in the child organization:  
  • Work center code
• Resource code
• A global standard operation can't be created in an item master org if electronic signatures are enabled for standard operations in the organization.
• A global standard operation can't be assigned to a child organization if electronic signatures are enabled for standard operations in the child organization.
• Assigning a global work definition using ADFdi and REST APIs is currently not supported.
• You can continue to create a standard operation directly in a child organization with no change in behavior.
• This feature is complementary to the 26B feature, **Redwood: Manage Global Work Definitions in an Item Master Organization**.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Manage Standard Operations (WIS_MANAGE_STANDARD_OPERATIONS_PRIV)
• View Standard Operations (WIS_VIEW_STANDARD_OPERATIONS_PRIV)
• Get Standard Operations by Service (WIS_GET_STANDARD_OPERATIONS_SERVICE_PRIV)
• Manage Standard Operations by Service (WIS_MANAGE_STANDARD_OPERATIONS_SERVICE_PRIV)
• Assign Global Standard Operations (WIS_PROPAGATE_GLOBAL_STANDARD_OPERATIONS)
• Unlink Replicated Standard Operation (WIS_UNLINK_REPLICATED_STANDARD_OPERATION)

The first four privileges were available prior to this update. The last two privileges are new in this update.

## 📚 Key Resources

• Watch the Manage Global Standard Operations in an Item Master Organization demo.
• Oracle Fusion Cloud SCM: Refer to the Using Manufacturing guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Refer to the Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Maintenance*