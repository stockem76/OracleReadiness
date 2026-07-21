[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Manufacturing](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/manufacturing.md)

# Redwood: Manage Tabular Data Efficiently in the Work Definition Pages

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/mfg26c/26C-mfg-wn-f44506.htm)

In this update, the Redwood Work Definition data grid pages have been enhanced to improve usability and data handling efficiency across the following pages: Operations, Operation Dependencies, Operation Outputs, Operation Items, Operation Resources, Instructions, and Parameters. The following capabilities have been added:

1. Column Sorting 
  • You can sort on key columns of type numeric and text.
2. Copy & Paste 
  • You can perform copy and paste using the keyboard shortcuts Control+C and Control+V at the cell level.
• You can copy and paste between data grid cells or from the data grid to another software application and vice versa.
3. Row Insertion via Context Menu 
  • You can now perform Insert Row Above and Insert Row Below using right-click context menu options.
4. Export to Excel 
  • You can now export the data in a data grid to Microsoft Excel.

Row Insertion Using the Context Menu

Export to Excel

These enhancements improve user productivity by enabling faster data entry and intuitive grid interactions. Additionally, the export capability facilitates data analysis and reporting.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• The columns exported to Excel are based on the sequence returned by the REST API and may not match with the columns displayed in the user interface.

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