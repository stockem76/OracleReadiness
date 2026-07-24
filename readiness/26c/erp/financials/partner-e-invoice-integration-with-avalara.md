[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Partner E-Invoice Integration with Avalara

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f50121.htm)

There is a global regulatory trend towards e-invoicing and continuous transaction controls, as governments seek to drive operational efficiency and reduce tax leakage. Businesses operating across multiple countries face significant challenges:

• Processing e-invoices from suppliers worldwide, each using different standards
• Interfacing with the various service providers
• Maintaining compliance with diverse regulations

Traditionally, this required organizations to manually set up connectivity parameters, exchange credentials, and conduct integration testing with one or more service providers. To help simplify these complexities, businesses need a robust, scalable solution that streamlines connectivity and ensures reliable compliance.

The preconfigured integration with Avalara helps organizations to comply with global e-invoicing mandates while improving operational efficiency. Customers can receive e-invoices from suppliers using various service providers and government platforms. The solution leverages a predefined mapping to transform the e-invoice received in a standard format from Avalara into the Payables invoice format.

In this release, the solution provides turnkey onboarding for the Avalara e-invoicing integration, receipt of e-invoices in supported countries, and automated acknowledgments to suppliers for processed and rejected invoices.

The integration with Avalara provides numerous benefits for businesses:

• Rapid onboarding of e-invoicing partner without the need for custom development or complex integrations.
• Regulatory compliance with e-invoicing mandates in supported countries.
• Improved operational efficiency through automated, standardized e-invoice processing.

## ⚙️ Steps to Enable and Configure

Before enabling e-invoicing with Avalara in Oracle Fusion Cloud ERP, ensure that the following prerequisites are completed:

1. Finalize agreement with Avalara  for using e-invoicing solution. You may have to provide the details of the participating legal entities such as name, address and registration number to Avalara.
2. Provision the buyer account using the Avalara  portal.
3. If operating in a PEPPOL country, then complete buyer registration on the PEPPOL network through Avalara.

**Steps for enabling connectivity with Avalara**

  Follow the steps below to establish a secure connection between Oracle Cloud ERP and Avalara. All credentials are exchanged using encrypted protocols.

  First, assign the security privilege to the administrator who manages the connectivity with Avalara.

1. Login as the IT Security Manager and navigate to the Security Console.
2. Create a custom job role.
3. In the Function Security Policies tab, add the privilege “Manage Avalara E-invoicing” and proceed to save the role.
4. Assign the newly created custom job role to the administrator user.

Then, follow these steps to create a connection to the Avalara e-invoicing service.

1. Sign into Oracle Cloud ERP as an administrator and go to Navigator > My Enterprise > Setup and Maintenance.
2. From the Setup and Maintenance work area, go to the Manage Avalara E-invoicing task. 
  • Offering: Financials
• Functional Area: Transaction Tax
• Task: Manage Avalara E-invoicing

Manage Avalara E-invoicing in Setup and Maintenance

1. Select Payables and click on Activate to initiate the connection.

Activate E-invoicing with partner

1. You will be redirected to Avalara’s portal to authorize data access. Login by entering the portal credentials provided by Avalara.

Login to Avalara portal

1. Provide consent if prompted for enabling the data flow from Avalara to Oracle Cloud ERP.
2. You will be redirected back to Oracle Cloud ERP.
3. Avalara and Oracle will establish a secure connection automatically and prepare the service for use through secure credentials exchange in the background.
4. You can view the status of the service by clicking on the View Activation Status button.
5. Once the enablement process is complete, the status is updated to Completed.

Connectivity completed

**Steps for supplier onboarding**

1. First, identify the suppliers for e-invoicing and notify them about e-invoicing capability. Share the details required for transmitting e-invoices via Avalara. This includes: 
  • Identifiers like Tax registration number and PEPPOL ID
• Service provider name (Avalara)
• Connectivity details like end points, credentials, signature, and protocols.
• The specific details to be shared depends on the country and model they are operating in. You can contact Avalara for additional guidance on supplier outreach.
2. The supplier can then register with an e-invoicing service provider to send invoices electronically. 
  • If the supplier doesn’t have a service provider for e-invoicing, they can either register with Avalara or another service provider which has interoperability agreement with Avalara.
• Suppliers then communicate their readiness to transition to e-invoicing and provide the required details like their tax registration number.
3. Finally, update the supplier’s tax registration numbers in Oracle Cloud ERP to ensure correct e-invoice processing. 
  • Navigate to Procurement > Supplier > Transaction Tax > Tax Registrations. 
    • Enter the tax registration number for the supplier.

Supplier Tax Registration Number

• Alternatively, use the supplier FBDI spreadsheet to update tax registration numbers of suppliers in bulk.

## 💡 Tips and Considerations

• Ensure that the tax registration numbers are correctly updated in the Legal Entity and Legal Reporting Unit, and the same details are shared with Avalara. This will ensure that the legal entity is correctly defaulted on the invoice.
• Ensure that the supplier tax registration number is updated in the supplier profile so that the correct supplier can be identified.

## 🔐 Access Requirements

You must have the Manage Avalara E-invoicing privilege to establish connectivity with Avalara.

## 📚 Key Resources

Guidelines for Configuring Security in Oracle ERP Cloud

---
*Oracle Cloud Readiness · 26C · ERP · Financials*