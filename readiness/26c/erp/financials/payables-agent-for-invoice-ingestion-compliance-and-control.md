[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Payables Agent for Invoice Ingestion, Compliance and Control

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49574.htm)

The Payables Agent delivers automation and industry best practices across the entire invoice lifecycle, enabling near-touchless processing. By drastically reducing manual intervention, organizations minimize processing errors, maximize operational efficiency, and empower finance teams to refocus on strategic activities. Over time, the Payables function shifts from a traditional cost center to a value-generating engine driving faster cycle times, capturing early payment discounts, and preventing capital leakage through advanced exception management and anomaly detection.

Powered by Generative AI, the Payables Agent automates invoice ingestion, compliance, and control across disparate sources and document formats. It supports multilingual recognition, natively integrates with global e-invoicing providers, and leverages enhanced image recognition to streamline the capture of complex, multi-format, and multi-page invoices. This touchless experience is built on a foundation of unified ingestion, automated processing, intuitive exception workflows, and straight-through processing from data capture to payment readiness. By replacing manual, fragmented, and reactive tasks with automated data enrichment, robust compliance controls, and seamless supplier collaboration, organizations achieve accelerated processing timelines, comprehensive operational visibility, and optimized financial outcomes.

Building on this touchless framework, in this release Payables Agent introduces Compliance and Control, a unified capability that brings automated invoice completion together with built-in compliance and control enforcement in a single experience. Using natural language processing, the Agent reads your existing business policy documents, understands the intent behind them, and automatically generates the corresponding application policies, replacing the manual setup that this traditionally required. During invoice processing, the Agent applies these policies to every invoice. It automatically fills in missing details such as account combinations, tax determinants, and project information, while at the same time running intelligent checks to identify and isolate transactions that fall outside your defined business criteria. Adaptive learning further extends this capability across all invoice attributes, including additional fields such as Descriptive Flexfields and Localization fields, which can be trained once and then applied automatically to invoices going forward, and also expands supplier invoice ingestion from custom XML and CSV file formats with minimal manual intervention.

**Key Capabilities**

Capabilities | Experiences
Payables Home Page | The Payables Agent home page provides a unified landing experience for users to interact with the Payables Agent, review prioritized insights, ask questions, use suggested prompts, and navigate to related Payables work areas.
Insights | Payables insights provide a prioritized view of open payables signals so users can quickly understand which invoices and processing activities need attention.
Capture Configurations | Define configurations for Document Receiving Endpoints and Stream configuration definitions. Configure endpoints, email aliases, and other key details to support Invoice ingestion.
Compliance and Control | The Compliance & Control (C&C) architecture marks a shift from manual ERP setup to an Agent-centric orchestration model.
Streams | Monitor real-time visibility into invoice ingestion of streams with up-to-date processing statuses to review overall health of touchless operations. Review document capture review to view individual invoice detailed processing steps and results to accelerate understanding and actions taken on invoice ingestion and control.
Onboarding New Format- Training | Access from the Streams page to upload new or review existing Invoice layouts for training and review the training status.
Invoice List | View all invoice management tasks, including both exception handling and querying on one place. View all invoices and statuses in a central hub , verify exceptions, and take the appropriate action on them.

**Payables Home Page**

The Payables Agent provides a single, AI-powered workspace for users to access Payables insights, ask questions, launch guided inquiries, and navigate to related Payables tasks. By combining conversational assistance, suggested prompts, and prioritized insights in one place, the Home page helps users quickly identify issues, access relevant information, and take action more efficiently. To improve productivity and adoption, the page simplifies navigation by giving users a consistent agentic entry point for Payables work. The experience also offers direct navigation to related Payables pages, reports, and business processes based on users' existing security access.

Payables Agent Home Page

**Insights**

Payables Insights delivers a proactive, insights-driven experience that helps Accounts Payable teams focus on the most important issues requiring attention. Instead of manually reviewing invoice lists and monitoring multiple work areas, users receive prioritized insights that highlight operational risks and processing exceptions from a centralized Payables Agent experience. The solution provides visibility into key areas such as invoice anomalies, processing exceptions, rejected invoices, and invoice backlogs. Each insight includes contextual information and recommended actions, enabling users to quickly understand the issue and navigate directly to the appropriate Payables workflow for investigation and resolution.

By surfacing critical issues earlier and prioritizing work based on urgency, Payables Insights helps organizations improve operational efficiency, strengthen controls, and support a more proactive and touchless invoice processing experience.

Actionable Insights

**Configurations for Capture**

For Invoice Image Documents stream, user can now do actions from Stream tab such as:

• **Alias Email Business Unit Mapping**: Users can now associate a Business Unit with an alias email address, enabling automatic Business Unit defaulting for unmatched invoices.
• **Requester Email Domain**: The invoice requester can now be automatically identified from the invoice document by recognizing the requester’s email address when available on the invoice. To enable this capability, enter your organization’s domain name in the Requester Email Domain configuration.

**Compliance and Control**

**Configuration Steps**

Setting up application rules traditionally required users to manually enter business logic based on internal processes and operating documents. The Compliance & Control (C&C) architecture replaces this manual setup with an AI-driven experience. Users can upload a document that contains their policy and policy details, and the Payables Agent reads the uploaded document, understands the business intent, and converts it into the appropriate application rules. All rules are generated based on the content of the uploaded policy document.  The C&C architecture relies on two core elements:

• **Policy:** Defines the overarching structure, purpose, and rules of your business requirements.
• **Policy Details:** Holds the specific values and conditions for each policy. The system evaluates these details whenever an invoice is created.

**How Policies are applied during Invoice Processing**

Once policies are generated from the uploaded policy document, the Payables Agent enforces them automatically at every stage of invoice processing, with no manual triggering or individual configuration required for each invoice. As an invoice is ingested or created, the Agent evaluates it against the active Compliance and Control policies before the invoice is finalized. Completion policies are applied first, where the system derives and populates any missing internal attributes such as account combinations, tax determinants, project costing, asset details, localization fields, and Descriptive Flexfields, based on the conditions defined in the corresponding Policy Details. Control policies are then enforced within the same processing pass, where each invoice is screened against the defined anomaly criteria and validated against related purchase orders or receipts. Any transaction that deviates from policy is automatically flagged and isolated for review. Because this evaluation runs consistently on every invoice, rather than as a one time or sampled check, compliance is applied uniformly across all transactions. The same business rules govern each invoice the moment it enters the system, ensuring that no invoice progresses without being assessed against the established policies.

**Invoice Completion**

Invoice Completion enables customers to intelligently derive internal attributes that are not explicitly provided on supplier invoices. In many scenarios, key transactional details such as accounting distributions, tax determinants, project costing information, asset information, country specific requirements, or additional information attributes required for reporting and compliance are not present in the source invoice data. This capability ensures such attributes are automatically determined during invoice processing, reducing dependency on manual intervention and completing the invoice in a touchless manner. The system interprets the user-defined policy and automatically generates the underlying logic, which is then consistently applied whenever invoices are processed. This simplifies invoice completion policy creation, accelerates implementation, and makes policy maintenance more accessible to business users.

**Invoice Control**

Controls consists of the following:

• Anomalies
• Document Processing Options

**Anomalies**

Anomalies are control mechanisms that automatically detect and flag invoices deviating from defined criteria for review. The feature provides automated, real-time risk management by systematically detecting and flagging invoices that deviate from established business criteria. As operations scale toward Touchless Payables, this feature enforces strict process compliance, proactively preventing financial fraud and processing errors before they impact the business.

**Document Processing Options**

It help automate how supplier invoice images are read, interpreted, and converted into Payables invoices. They control recognition of key invoice details such as tax, freight, invoice lines, service orders, utility suppliers, and miscellaneous charges. These options also guide import behavior, including incomplete invoice creation, paired line import, and tax calculation during import. They support validation of critical information such as legal entity for PO matched invoices. Overall, they reduce manual effort, improve invoice capture quality, and ensure consistent, compliant invoice processing.

**Onboarding New Format-Training**

The enhanced **Invoice Document Training** experience provides a guided workspace for improving invoice document processing across both structured and unstructured document formats. Customers can now review extracted invoice data, identify mapping gaps, provide correction instructions, and continuously train the system to improve future invoice processing accuracy.

For structured invoice formats such as XML (UBL, OAG 7.0, OAG 10.0, Custom XML) and CSV (including flat tables with invoice header and invoice lines in same sheet or zipped file two CSV file one for Invoice header and other for invoice Lines) users can provide natural-language mapping and transformation instructions directly within the application. The experience includes visibility into unmapped source attributes, missing mandatory invoice attributes, and a preview of how source data maps to Oracle Fusion Payables invoice attributes. Users can also upload instruction documents, define transformation rules, and validate results before applying changes.

**Training Capabilities for all Invoice Attributes including Descriptive and Global Flexfields**

The enhanced training capability to support training across all invoice attributes for both structured documents (such as CSV and XML files) and unstructured documents (such as PDF, JPEG, and PNG files). During training, all labelled attributes are extracted from source documents and can be mapped to any of the invoice attributes, including Descriptive Flexfields (DFF) and Global Descriptive Flexfields (GDF), which were not previously supported. This enhancement enables organizations to train customer-specific business attributes captured through DFFs as well as country-specific localization and compliance attributes captured through GDFs. Training provided by users is saved as learning data and automatically applied to subsequent invoice documents. This reduces repetitive manual intervention, improves field-level accuracy over time, and helps streamline downstream invoice processing.

**Invoice Document Streams- Support for additional file format like CSV and XML**

Invoice Creation from custom XML and CSV enable AP teams to ingest supplier invoice data from varied CSV formats and convert it into Payables invoices with minimal manual effort. The capability supports different file layouts, including flat tables with invoice header and invoice lines in same sheet or zipped file two CSV file one for Invoice header and other for invoice Lines, while using Gen AI to interpret file structure and map the source document attribute to fusion defined payables invoice attributes. This provides a unified intake path for structured invoice data and helps transform inconsistent supplier files into valid, auditable invoice records.

**Invoice List**

The Invoice page is a powerful, centralized hub that transforms traditional invoice management, exception handling, and query resolution into an intuitive, AI-driven experience. Replacing manual filters with a streamlined, split-screen interface, the page is divided into two core functional areas:

• **The AI Chat Window (Left):** The primary interaction point where users engage with an intelligent agent. Instead of manually configuring filters, users simply converse with the agent to query data, call up specific invoices, or request status updates.
• **The Action Canvas (Right):** A dynamic display area where the agent renders real-time results, invoice details, and flagged exceptions.

Through this conversational workflow, users can seamlessly verify violations, resolve invoice rejections, override anomalies, or make required corrections directly on the canvas—making invoice management faster, smarter, and entirely hands-free.

**Business Benefit Includes:**

Payables Agent 26C introduces new AI-driven capabilities that help organizations accelerate invoice processing, improve operational visibility, strengthen compliance, and increase automation across the invoice lifecycle. By combining intelligent document ingestion, continuous learning, proactive insights, automated controls, and conversational experiences, customers can reduce manual effort, improve invoice data quality, and enable higher levels of touchless invoice processing.

Key benefits include:

• Increase automation through intelligent invoice capture, enrichment, and processing.
• Increase automation through enhanced training capabilities that support all invoice attributes, including Descriptive Flexfields (DFF) and Global Descriptive Flexfields (GDF), across both structured and unstructured invoice formats.
• Reduce manual intervention with AI-assisted learning, policy configuration, and exception management.
• Improve invoice accuracy and data quality through continuous learning and automated validation.
• Strengthen compliance and financial controls with anomaly detection, policy-driven governance, and targeted review mechanisms.
• Accelerate issue identification and resolution through proactive insights and guided recommendations.
• Enhance user productivity with conversational experiences and a unified Payables workspace.
• Improve operational visibility into invoice processing performance, exceptions, and risks.
• Support scalable supplier onboarding through flexible document ingestion and transformation capabilities.
• Increase touchless invoice processing rates while maintaining auditability and control.
• Expand supplier invoice automation by supporting invoice ingestion from custom XML and CSV file formats with minimal manual intervention.

## ⚙️ Steps to Enable and Configure

**Feature Enablement**

This feature is enabled by default. After the required security roles and privileges described in Access Requirement section are configured, users can access the feature through the new **“Payables Agent”** navigation entry.

## 💡 Tips and Considerations

**Payables Home Page**

• Saved and recent prompts are limited to conversations initiated directly from the Home page.
• Users can skip optional attributes in predefined syntax prompts. The agent will still interpret the request using available defaults or broader results.
• Navigation destinations remain security-controlled, and if a user selects a destination they can't access, the experience displays an access error.
• When the navigation destination is from a submitted prompt as a part of the agent experience, it opens in an in-application tab; when the destination is a navigation to a specific task, report, or process, it opens in a new browser tab so users can return to the Home page without losing their place.
• Insight cards only display for those related to the Invoices context, and are prioritized so users can focus first on the most urgent and recent items.

**Insights**

• Seeded monitoring prompts are delivered by Oracle and enabled by default.
• Users can pause future evaluations by disabling a prompt, while previously generated insights remain available for reference.
• Duplicate monitoring prompts let users adjust execution behavior, such as frequency, time frame, and priority.
• Disabling a duplicate prompt stops future evaluations for that duplicate, but doesn’t delete historical insights.
• Insights are shown based on the user’s access, so users must have access to the Insights page and the related monitoring prompt actions.
• The specific insights and data visible to a user depend on their assigned privileges and data security access.
• If no open insights match the current filters, the page displays a message indicating that the user’s insights are clear.

**Anomalies**

• Determine Organizational Priorities: Focus anomaly pattern criteria on conditions meaningful to your organization's policies and controls. For stricter enforcement, define longer historical time periods and lower variation percentages across patterns to achieve more stringent control.
• Test Before Broad Rollout: Validate anomaly patterns are being applied as expected and in a manner consistent with your organization's controls and policies in a controlled environment before full-scale operational deployment.

**Invoice Completion**

• Invoice completion policies can be either for Invoice Header level attributes or Line level attributes or some installment attributes.
• Invoice completion policies will default a value if there is no attribute present on the record. If there is already a value in the field, then attribute defaulting will not override the same.
• Invoice completion policies apply during import, and no invoice completion policy applies for Manually created invoices or invoices directly created in AP base tables.

**Document review Criteria**

• It should be clearly configured to pause stream processing when documents require user review, using seeded, extendable, user-enabled, or user-defined rules.
• It can be applied at the file/document level for Stream Specialist review.
• It applies during both runtime processing, and should be treated separately from exception handling since it is a review-control mechanism rather than an error condition.

**Onboarding New Format-Training**

• Ensure mandatory invoice attributes are correctly mapped to avoid processing exceptions and incomplete invoices.
• Use the Need Attention section to identify and resolve missing required attributes before invoice creation.
• Leverage natural language instructions for mapping and transformation rules to reduce manual configuration effort.
• Test mapping and transformation rules using representative supplier documents before applying them to large volumes of invoices.
• When onboarding new XML or CSV formats, review available source attributes and validate how they map to Oracle Fusion Payables invoice attributes.
• Use the Preview experience to verify mapped values, transformed attributes, and newly created invoice lines before submitting training updates.

**Invoice Document Streams**

• Validate supported custom XML and CSV layouts, before enabling the feature for suppliers or business partners.
• Ensure mapped invoice attributes are reviewed for accuracy, especially where suppliers use non-standard headers, naming conventions, or custom column structures.
• Establish controls for file ownership, upload access, audit tracking, and approval responsibilities to maintain compliance and traceability.

**Invoice List**

• Utilize Conversational Workflows**:** Maximize efficiency by treating the Payables Agent as a digital colleague. Instead of just asking for data, use the chat window to engage in a continuous dialogue to guide you through multi-step invoice reviews and action workflows.
• Leverage Spreadsheet Corrections for Bulk Imports: For invoices rejected during the import process, rely on the integrated, intuitive correction spreadsheet to quickly pinpoint data errors and perform clean-up tasks before re-submitting.
• Execute Immediate Exception Actions: When the agent highlights an invoice exception on the canvas, resolve it immediately. You can cancel the invoice, release the exception if it is a false positive or navigate to the Edit page to update incorrectly captured data.
• Verify Anomalies**:** Use the right-side canvas to visually review the specific data points flagged by the agent's anomaly detection controls before deciding to override or release it.

## 🔐 Access Requirements

Access to new feature components and pages are managed through specific security artifacts tailored to the underlying design requirements. This section offers a consolidated view of these controls, including the privileges and roles required to grant access to the relevant pages. Make sure you’ve finished all necessary prerequisites; For detailed instructions and reference materials, refer to the document listed in the Key Resources section.

Component Name | Component Type | Security Details
Artifact Name | Artifact Type | Security View
Payables Home Page | Page | Payables Invoice Processing Duty | SAS Duty Role | 
Manage Payables Invoice List Activities | Privilege | 
Insights | Page | Payables Agent Insights Duty | SAS Duty Role | 
Review Payables Agent Monitoring Prompt Duty | SAS Duty Role | 
Payables Agent Monitoring Prompt Management Duty | SAS Duty Role | 
Payables Agent Monitoring Prompt Administration Duty | SAS Duty Role | 
Payables Invoice Processing | SAS Duty Role | 
Payables Administration Duty | SAS Duty Role | 
Financials Intelligent Agent Runtime Duty | OPSS Duty Role | 
Financials Intelligent Agent Runtime Duty | OPSS Duty Role - HCM | 
Access Payables Agent Insights | Privilege | 
Review Payables Agent Monitoring Prompts | Privilege | 
Manage Payables Agent Monitoring Prompts | Privilege | 
Administer Payables Agent Monitoring Prompts | Privilege | 
Manage Payables Invoice List Activities | Privilege | 
Manage Payables Compliance and Control | Privilege | 
Configuration - Capture, Compliance & Control | Page - Edit | Financials Intelligent Agent Runtime Duty | OPSS Duty Role | 
Financials Intelligent Agent Runtime Duty | OPSS Duty Role - HCM | 
Fai Genai Agent Runtime Duty | SAS Duty Role | 
Manage Payables Document Capture | Privilege | 
Manage Payables Compliance and Control | Privilege | 
Manage Attribute Derivation Rules | Privilege | 
oraErpCoreDocumentIntegration_DocumentIntegrationStreamDefinition_read | Permission Group | AllRowsAllFields
oraErpCoreDocumentIntegration_DocumentIntegrationChannel_read | Permission Group | AllRowsAllFields
oraErpCoreDocumentIntegration_DocumentIntegrationChannel_update | Permission Group | AllRowsAllFields
oraErpCoreDocumentIntegration_DocumentIntegrationStreamCategory_read | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesIntelligentDocumentRecognitionOptionExtension_create | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesIntelligentDocumentRecognitionOptionExtension_read | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesIntelligentDocumentRecognitionOptionExtension_update | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesIntelligentDocumentRecognitionOptionExtension_delete | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesIntelligentDocumentRecognitionOption_read | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesIntelligentDocumentRecognitionOption_create | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesIntelligentDocumentRecognitionOption_update | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesIntelligentDocumentRecognitionOption_delete | Permission Group | AllRowsAllFields
oraErpCoreSensorPolicies_DataSensorPolicy_read | Permission Group | RowsForPayablesInvoiceAnomaliesAllFields
oraErpCoreSensorPolicies_DataSensorType_read | Permission Group | PayablesInvoiceAnomaliesSensorTypeRowAllFields
oraErpCoreSensorPolicies_DataSensorPolicy_update | Permission Group | RowsForPayablesInvoiceAnomaliesAllFields
oraErpCoreSensorPolicies_DataSensorPolicy_read | Permission Group | RowsForPayablesInvoiceMatchingControlsAllFields
oraErpCoreSensorPolicies_DataSensorPolicy_update | Permission Group | RowsForPayablesInvoiceMatchingControlsAllFields
oraErpCoreSensorPolicies_DataSensorPolicy_create | Permission Group | RowsForPayablesInvoiceMatchingControlsAllFields
oraErpCoreSensorPolicies_DataSensorPolicy_delete | Permission Group | RowsForPayablesInvoiceMatchingControlsAllFields
oraErpCoreSensorPolicies_DataSensorSchedule_read | Permission Group | AllRowsAllFields
oraErpCoreSensorPolicies_DataSensor_read | Permission Group | AllRowsAllFields
oraErpCoreSensorPolicies_DataSensorType_read | Permission Group | PayablesInvoiceMatchingControlsSensorTypeRowAllFields
oraErpCoreWorkflows_ErpWorkflowFact_read | Permission Group | RowsForPayablesInvoiceMatchingControlsAllFields
oraErpCoreWorkflows_ErpWorkflowObject_read | Permission Group | RowsForPayablesInvoiceMatchingControlsAllFields
oraErpCorePayablesSetup_PayablesInvoiceToleranceOption_read | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesInvoiceToleranceOption_create | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesInvoiceToleranceOption_update | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesInvoiceToleranceOption_delete | Permission Group | AllRowsAllFields
Configuration - Capture, Compliance & Control | Page - View | Financials Intelligent Agent Runtime Duty | OPSS Duty Role | 
Financials Intelligent Agent Runtime Duty | OPSS Duty Role - HCM | 
Fai Genai Agent Runtime Duty | SAS Duty Role | 
View Payables Document Capture | Privilege | 
View Payables Compliance and Control | Privilege | 
Review Attribute Derivation Rules | Privilege | 
oraErpCoreDocumentIntegration_DocumentIntegrationStreamDefinition_read | Permission Group | AllRowsAllFields
oraErpCoreDocumentIntegration_DocumentIntegrationChannel_read | Permission Group | AllRowsAllFields
oraErpCoreDocumentIntegration_DocumentIntegrationStreamCategory_read | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesIntelligentDocumentRecognitionOptionExtension_read | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesIntelligentDocumentRecognitionOption_read | Permission Group | AllRowsAllFields
oraErpCorePayablesSetup_PayablesInvoiceToleranceOption_read | Permission Group | AllRowsAllFields
oraErpCoreSensorPolicies_DataSensorPolicy_read | Permission Group | RowsForPayablesInvoiceAnomaliesAllFields
oraErpCoreSensorPolicies_DataSensorType_read | Permission Group | PayablesInvoiceAnomaliesSensorTypeRowAllFields
oraErpCoreSensorPolicies_DataSensorPolicy_read | Permission Group | RowsForPayablesInvoiceMatchingControlsAllFields
oraErpCoreSensorPolicies_DataSensorSchedule_read | Permission Group | AllRowsAllFields
oraErpCoreSensorPolicies_DataSensor_read | Permission Group | AllRowsAllFields
oraErpCoreSensorPolicies_DataSensorType_read | Permission Group | PayablesInvoiceMatchingControlsSensorTypeRowAllFields
oraErpCoreWorkflows_ErpWorkflowFact_read | Permission Group | RowsForPayablesInvoiceMatchingControlsAllFields
oraErpCoreWorkflows_ErpWorkflowObject_read | Permission Group | RowsForPayablesInvoiceMatchingControlsAllFields
Invoice Documents Streams | Page - Edit | Manage Supplier Invoice Stream | Privilege | 
read:Payables Document Stream Detail | Permission Group | All Rows and Unrestricted Fields
Invoice Documents Streams | Page - View | View Supplier Documents in Stream | Privilege | 
read:Payables Document Stream Detail | Permission Group | All Rows and Unrestricted Fields
Invoice Documents Training | Page - Edit | Manage Supplier Documents Training | Privilege | 
Invoice Documents Training | Page - View | View Supplier Documents Training | Privilege | 
Source File | Button | Download Payables Invoice Source Document | Privilege | 
Invoices | Page | Manage Payables Invoice List Activities | Privilege | 
Financials Intelligent Agent Runtime Duty | OPSS Duty Role | 
Financials Intelligent Agent Runtime Duty | OPSS Duty Role - HCM | 
Fai Genai Agent Runtime Duty | SAS Duty Role | 
Payables Invoice Processing Duty | SAS Duty Role | 
read:Business Unit | Permission Group | AllRowsAllFields
read:Currency | Permission Group | AllRowsAllFields
oraErpCoreSensorPolicies_DataSensorEntityTag_read | Permission Group | AllRowsAllFields
oraErpCoreSensorPolicies_DataSensorEntityTag_update | Permission Group | AllRowsAllFields
oraErpCoreSensorPolicies_DataSensorPolicy_read | Permission Group | AllRowsAllFields
oraErpCoreSensorPolicies_DataSensorPolicy_update | Permission Group | AllRowsAllFields
oraErpCorePayablesInvoices_PayablesInvoiceDistribution_read | Permission Group | MDABusinessUnitRowsUnrestrictedFields
oraErpCorePayablesInvoices_PayablesInvoiceHold_read | Permission Group | MDABusinessUnitRowsUnrestrictedFields
oraErpCorePayablesSetup_PayablesInvoiceHoldandReleaseCode_read | Permission Group | MDABusinessUnitRowsUnrestrictedFields
read:Payables Invoice Installment | Permission Group | AllRowsAllFields
Open Corrections Spreadsheet | Button | Correct Payables Import Validation Errors | Privilege |

**Data Security Access for Invoice List Page:**

  For the custom job role that grants access to the new Stream, List, and Graphic Equalizer pages, an additional step of Data Security Access is required. This custom job role (for Invoice List Page access) must have Business Unit access to that custom role.  If BU access is not granted, the user will not be able to see the invoice in the Invoice List page. Even when the user drill downs from the Stream page to the corresponding invoice on the Invoice List page, they will not be able to see it without the appropriate data security access.

  To configure this Data Security Access, you need to navigate to Manage Business Unit Data Access for Users, select the user name and the custom role created above, and grant access to the appropriate Business Unit, click Process Permission Group Policies to trigger the Permission Group Policies processing. Once this is completed, the user will be able to drill down from the Stream page to the Invoice List page, view the invoice, and search for invoices directly from the Invoice List page.

**Note:** Access to navigate to payables tasks, reports, or processes is governed by users' regular assigned OPSS security. No separate security is required for those navigation destinations.

## 📚 Key Resources

• **Reference Document** – Security Reference for Financials: Payments and Payables duties and privileges – Configuring Security in Oracle ERP Cloud

---
*Oracle Cloud Readiness · 26C · ERP · Financials*