[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Procurement](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/procurement.md)

# Integrate and Extend Procurement Using REST Resources

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/proc26c/26C-procurement-wn-f46407.htm)

In this release, Oracle Fusion Cloud Procurement and Oracle Fusion Cloud Self Service Procurement deliver new and modified REST resources to enable and simplify integration with external systems.

The new REST resource introduced in this update is:

• Draft Purchase Agreements
• Supplier Negotiations Calendar
• Supplier Negotiation Templates
• Seller Negotiations
• Seller Negotiation Bids
• Sourcing Programs
• Supplier Assessments
• Supplier Qualification Models

The following REST resources were previously available, and have been updated:

• Purchase Agreement Lines 
  • The following new child resources have been added: Flexfields for Lines, Flexfields for Item Attributes and Flexfields for Price Breaks.
• Supplier Negotiations
• Use the custom action Add Project Tasks to add project tasks from a project plan in Projects module to a negotiation.
• GET is supported for the Lines child resource to fetch the unique identifier of the source agreement associated with a negotiation line.
• Supplier Negotiation Purchasing Documents
• PATCH is supported to associate an inventory item to an awarded alternate line.
• Use the Create Staged Purchasing Documents custom action with the new attribute Purchasing Documents Creation Intent as Reset to re-create staged purchasing documents.
• Use the Create Staged Purchasing Documents custom action to specify whether to allow multiple legal entities in a single order or not.
• Negotiations in Supplier Portal
• GET is supported for the All Supplier Responseschild resourceto retrieve all supplier responses in a negotiation including competing responses from other suppliers in open and unsealed negotiations.
• Supplier Negotiations
• PATCH is supported for the Task Completion Date attribute in the Collaboration Team Members child resource to mark the collaboration team task as complete.
• Supplier Initiatives
• Use the new Initiative Assessments for Suppliers child resource to get the assessment details for suppliers.
• Use the new Internal Responders child resource to manage the default internal responders in survey initiatives.
• Use the new Internal Responders for Suppliers child resource to manage the internal responders for suppliers in survey initiatives.

You can use these new and modified REST resources to simplify integrations and support standards-based interoperability with your other applications and external systems.

## ⚙️ Steps to Enable and Configure

Review the REST service definition in the REST API guides to leverage (available from the Oracle Help Center > *your apps service area of interest* > APIs & Schema). If you are new to Oracle's REST services you may want to begin with the Quick Start section.

## 🔐 Access Requirements

Refer to the Privileges section in the REST API for Oracle Fusion Cloud Procurement documentation, available on the Oracle Help Center.

## 📚 Key Resources

Refer to the REST API for Oracle Fusion Cloud Procurement documentation, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Procurement*