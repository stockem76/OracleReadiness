[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Maintenance](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/maintenance.md)

# Use Expanded Description Fields for Work Orders and Operations

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/maint26c/26C-maintenance-wn-f46399.htm)

In this update, long description fields are added to support more detailed maintenance documentation and instructions with up to 4000 characters.

For standard operations, the long description field is enabled through business rules as needed. For maintenance work definitions, long descriptions are supported for both the work definition header and work definition operations. When you add a standard operation to a work definition, you can view and edit the long description for unreferenced standard operations. For referenced standard operations, you can only view the long description.

For maintenance work orders, you can add long descriptions to both work orders and work order operations. When you create a maintenance work order using a maintenance work definition, long descriptions from the work definition and work definition operations are carried forward to the corresponding work order and work order operations. Similarly, when you add a standard operation to a work order, the long description is copied to the work order operation. The long descriptions of work order and work order operations can be edited.

This enhancement is supported across user interfaces, REST services, and file-based data import (FBDI) processes for the applicable entities.

This feature helps organizations document maintenance activities, instructions, and supporting details with greater clarity and continuity across maintenance processes.

Improve maintenance execution and documentation quality by enabling detailed instructions and maintenance context across work definitions, standard operations, and work orders.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

For global work definitions assigned to multiple maintenance organizations, long descriptions aren't currently copied to the child organizations.

---
*Oracle Cloud Readiness · 26C · SCM · Maintenance*