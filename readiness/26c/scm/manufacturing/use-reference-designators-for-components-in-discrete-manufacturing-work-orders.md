[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Manufacturing](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/manufacturing.md)

# Use Reference Designators for Components in Discrete Manufacturing Work Orders

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/mfg26c/26C-mfg-wn-f44514.htm)

Electronics and complex assembly manufacturers commonly use components with positional information that is critical for correct manufacturing execution and traceability. A reference designator uniquely identifies a component within an assembly, so that it can be easily located in the item structure, documentation, and physical product. The positional identification is particularly important in scenarios where a component repeats multiple times for the same level of an item structure.

You can now install a component and record its reference designator during material issue or backflush for discrete manufacturing work orders. The reference designators defined for an item structure component are carried forward to the work order and work execution to guide issue, return, and verification tasks. The traceability between the reference designator for an installed component and its serialized assembly also facilitates audit, service, and quality investigations.

View Reference Designators for a Work Order Operation Material

Scan or Enter a Reference Designator when Reporting a Material Transaction

Enter a Reference Designator while Reporting a Material Transaction Post Production

Enter a Reference Designator While Reporting a Material Transaction Using a Handheld Device

You can also record reference designators while reporting a material transaction using REST, ADFdi, and FBDI.

View Reference Designators in Production Transaction History

View Reference Designator in Product Genealogy

Recording reference designators in manufacturing execution provides the following benefits:

• Enhances manufacturing accuracy by guiding operators with the correct placement.
• Improves quality, compliance, and audit readiness.
• Simplifies troubleshooting when defects are tied to specific designator positions.

*Here's the demo of these capabilities:*

## ⚙️ Steps to Enable and Configure

Set up the plant parameter to enable this feature:

1. In the Setup and Maintenance work area, search for, and select the **Manage Plant Parameters** task.
2. On the Manage Plant Parameters page, select the required inventory organization.
3. In the **Work Execution** tab, under **Execute Production**, select the **Use reference designators in discrete work order execution**checkbox.

Enabling the Plant Parameter

## 💡 Tips and Considerations

• This feature applies only to discrete manufacturing and isn't supported for process manufacturing, orderless execution, or flow schedule execution.
• The reference designators are not carried forward from item structures to work definition operations.
• You can't pick and issue material directly for a work order operation when a reference designator is required.
• You can't enter reference designators while reporting negative material issues and returns, operation scrap, and return from scrap.
• As a best practice, you can use a reference designator for unique identification of component position or physical location within the assembly, while using the Find Number for quick reference to an indexed engineering drawing.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains the following privileges can access this feature:

Manage Plant Parameters (RCS_PLANT_PARAMETERS_PRIV)

Manufacturing privileges

• Manage Work Order Headers (WIP_MANAGE_WORK_ORDER_HEADERS_PRIV)
• View Work Orders (WIP_VIEW_WORK_ORDERS_PRIV)
• Report Material Transactions (WIP_REPORT_MATERIAL_TRANSACTIONS_PRIV)
• View Production Transaction History (WIE_VIEW_MANUFACTURING_TRANSACTION_HISTORY_PRIV)
• Report Postproduction Transactions (WIE_REPORT_POSTPRODUCTION_TRANSACTIONS_PRIV)
• Review Product Genealogy (CSE_REVIEW_PRODUCT_GENEALOGY_PRIV )

These privileges were available prior to this update.

## 📚 Key Resources

• Watch the Use Reference Designators for Components in Discrete Manufacturing Work Orders demo.
• Refer to the Oracle Fusion Cloud SCM: Using Manufacturing guide, available on the Oracle Help Center.
• Refer to the Oracle Fusion Cloud SCM: Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Manufacturing*