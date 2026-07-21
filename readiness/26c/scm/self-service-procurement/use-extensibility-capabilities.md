[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Self Service Procurement](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/self-service-procurement.md)

# Use Extensibility Capabilities

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/ssproc26c/26C-ssproc-wn-f46537.htm)

You can now use the extensibility capabilities supported in the Redwood Self Service Procurement application. With this update, you can extend the application in these areas:

• Home Page 
  • Personalize the Additional information drawer for preparers, requesters, buyers, and approvers. 
    • Show or hide one or more attributes within the drawer.
• Enable or disable the person link.
• Enable or disable the location link.
• Disable policy evaluation and noncatalog request creation in the Purchase Requisition Creation agent using the *Self Service Procurement AI Agent Input Context* constant.
• Configure the *Create Requisition from Supplier Quote AI Agent Code* constant to enable the *Quote to Purchase Requisition Assistant from Menu* feature.
• Show or hide the in-app navigation using the *Show Navigation on Create Requisition Pages*constant.
• Enable the *Search for Deliver-to Locations Using Additional Attributes in Requisitions* feature using Enable the Enhanced Deliver-to Location LOV constant.
• Enable the *Access Noncatalog Request from the Actions Menu on the Home Page* feature using the Show Create Noncatalog Request constant.

• Manage Public Shopping Lists 
  • Personalize Create public shopping list drawer fields.
• Personalize the table layout.
• Add a Guided Journey.
• Add or Edit Public Shopping List 
  • Personalize the Additional information drawer for buyers. 
    • Show or hide one or more attributes within the drawer.
• Personalize the Add from Catalog table.
• Personalize the Lines table.
• Add a Guided Journey.

## ⚙️ Steps to Enable and Configure

Leverage the Visual Builder Studio to expose your applications. To learn more about extending your application using Visual Builder, visit Oracle Help Center > *your apps service area of interest* > Books > Configuration and Extension.

## 💡 Tips and Considerations

Extensibility is limited to the features described in the Extending the Redwood Self Service Procurement Application document. Don't make other extension changes because they aren't compatible with future updates and might cause pages to render incorrectly.

## 📚 Key Resources

• To know more about the extensibility, refer to the Extending the Redwood Self Service Procurement Application document.
• For information about using Oracle Visual Builder Studio to extend your Redwood application pages, see Oracle Fusion Cloud HCM and SCM: Extending Redwood Applications for HCM and SCM Using Visual Builder Studio.

---
*Oracle Cloud Readiness · 26C · SCM · Self Service Procurement*