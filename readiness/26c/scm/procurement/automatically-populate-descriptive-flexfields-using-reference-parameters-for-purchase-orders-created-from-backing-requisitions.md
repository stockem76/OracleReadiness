[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Procurement](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/procurement.md)

# Automatically Populate Descriptive Flexfields Using Reference Parameters for Purchase Orders Created from Backing Requisitions

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/proc26c/26C-procurement-wn-f43879.htm)

Automatically populate descriptive flexfields, including Project descriptive flexfields, using reference parameters when creating purchase orders from backing requisitions. Before this update, the application could automatically populate these flexfields only when creating purchase orders without a requisition.

You can use these reference parameters to default descriptive flexfields on purchase orders created from backing requisitions:

• Header: SoldtoLegalEntityId, ProcurementBUId, SupplierId, SupplierSiteId, RequisitioningBUId, DocumentType, DocumentStyleId
• Lines**:** SoldtoLegalEntityId, ProcurementBUId, SupplierId, RequisitioningBUId, DocumentType, DocumentStyleId, SupplierSiteId, LineTypeId, SourceAgreementId, CategoryId, ItemId
• Schedules**:** SoldtoLegalEntityId, ProcurementBUId, SupplierId, RequisitioningBUId, DocumentType, DocumentStyleId, SupplierSiteId, LineTypeId, SourceAgreementId, CategoryId, ItemId, ShipToOrganizationId
• Distributions**:** SoldtoLegalEntityId, ProcurementBUId, SupplierId, RequisitioningBUId, DocumentType, DocumentStyleId, SupplierSiteId, LineTypeId, SourceAgreementId, CategoryId, ItemId, ShipToOrganizationId, RequesterId

You can use these reference parameters to default project descriptive flexfields on purchase orders created from backing requisitions**:**

• RequisitioningBUId, RequestedDeliveryDate, CategoryId, RequesterId, DestinationTypeCode, InventoryItemId.

**Example 1**: Default a purchase order header descriptive flexfield using the SoldtoLegalEntityId reference parameter when the requisition doesn’t include a descriptive flexfield value.

Purchase Order Header Descriptive Flexfield Setup Using SoldtoLegalEntityId as the Reference Parameter

Requisition with Empty Header Descriptive Flexfield

Purchase Order Header Descriptive Flexfield  Is Defaulted Based on SoldtoLegalEntityId

**Example 2**: Default the Expenditure Type project descriptive flexfield using the InventoryItemId reference parameter when the requisition doesn’t include a project descriptive flexfield value.

Project Descriptive Flexfield Setup Using InventoryItemId as the Reference Parameter

Requisition with No Project Descriptive Flexfield Value

Purchase Order Project Descriptive Flexfield Showing a Default Value Based on InventoryItemId

## ⚙️ Steps to Enable and Configure

You must create and enable the PO_ENABLE_PO_DFF_DEFAULTING_FOR_BACKING_REQS  profile option to access this feature.

• To create the profile option, follow the steps in the Create and Edit Profile Options topic.
• After you have created the profile option, follow these steps to enable it: 
  • In the Setup and Maintenance work area, search and select the **Manage Administrator Profile Values**task.
• On the **Manage Administrator Profile Values**page, search for and select the profile option name or code.
• In the Profile Values section, set the Site level to **Yes**.
• Click **Save** and **Close**. Changes in the profile value will affect users the next time they sign in.

## 💡 Tips and Considerations

• Descriptive flexfields on purchase orders created from backing requisitions are defaulted only when this feature is enabled and one of these conditions is met: 
  • Requisition flexfield values aren’t provided, or
• Requisition flexfields have values, but the application isn't configured to copy the requisition flexfield values to purchase orders.
• Project descriptive flexfields on purchase orders created from backing requisitions are defaulted only when this feature is enabled and the requisition doesn't have a value for project descriptive flexfields.

## 🔐 Access Requirements

No specific privileges are required to default descriptive flexfields and project descriptive flexfields on purchase orders created from backing requisitions by using reference parameters.

---
*Oracle Cloud Readiness · 26C · SCM · Procurement*