[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Maintenance](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/maintenance.md)

# Manage Organizations for Global Work Definitions Using File-Based Data Import

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/maint26c/26C-maintenance-wn-f46394.htm)

Work definitions are defined at the maintenance organization level based on organization-specific work areas, work centers, material items, and resources. In this update, if you have work definitions with the same scope across multiple maintenance organizations, you can manage them globally.

In the previous update, you could create and assign global work definitions to child organizations using the Redwood **Work Definitions** page. In this update, you can use file-based data import (FBDI) to create and assign global work definitions across child organizations.

The **Maintenance Work Definition** template now includes the **Replicate Global Work Definition Flag** column in the worksheet. When you specify **Yes** while creating a work definition in an item master organization, the work definition is created as a global work definition and automatically assigned to child organizations where validations pass. If you specify **No**, the work definition is created without automatic assignment, and you must manually assign it to child organizations using the Redwood **Work Definitions** page.

Updates made to global work definitions using the template aren't automatically synchronized across child organizations. After making updates, you must use the Redwood **Work Definitions** page to manually synchronize changes to child organizations.

Reduce maintenance effort and improve consistency by managing and assigning global work definitions across multiple maintenance organizations using file-based import capabilities.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Manufacturing and Supply Chain Materials Management*  No Longer Optional From: *Update 26D*

Download and review the latest Maintenance Work Definition template in the File-Based Data Import for Oracle Supply Chain Management Cloud guide available on the Oracle Help Center. To import data using the template, follow the instructions in the Load Data into Tables topic.

## 💡 Tips and Considerations

If you don't want a newly created global work definition to synchronize automatically to all child organizations, use the Redwood **Work Definitions** page to selectively assign the work definition after creation to specific child organizations.

---
*Oracle Cloud Readiness · 26C · SCM · Maintenance*