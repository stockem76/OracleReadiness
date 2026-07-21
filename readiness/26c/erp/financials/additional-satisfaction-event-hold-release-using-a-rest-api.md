[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Additional Satisfaction Event Hold Release Using a REST API

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f47243.htm)

Use the Additional Satisfaction Events REST API to release revenue on performance obligations by recording the completion of customer acceptance, payments, or service provisioning events.

This REST service provides a scalable alternative to the File-Based Data Import approach, enabling organizations to integrate customer acceptance, proof of delivery, payment, or service provisioning events to release holds on performance obligations.

You can call the API during standard revenue processing to create and query additional satisfaction events. When creating an event, the system validates that all required fields are completed, including source document type, source system, fulfillment date, event type, and unique identifiers for both the additional satisfaction event and the related source document line. If required information is missing or the referenced source document line is invalid, the request is rejected with a clear, actionable error message.

The API verifies that the source document line has a status of Processed and enforces the same business rules used for additional satisfaction event processing. It applies the appropriate validations based on the satisfaction measurement model and event type, ensuring that only valid events are recorded and used to release revenue recognition holds.

Additional satisfaction events submitted through the REST API can be queried directly through the service, enabling seamless integration with external systems.

Update and delete operations are not currently supported.

Business benefits include:

• Enables scalable, API driven integration for organizations managing high volumes of additional satisfaction events.
• Reduces manual effort and eliminates dependency on FBDI based import processes.
• Improves accuracy and consistency by enforcing required validations during event creation.
• Accelerates the release of revenue recognition holds when customer acceptance, proof of delivery, payment or service provisioning events are completed.
• Enhances auditability and operational efficiency through direct system to system processing.

## ⚙️ Steps to Enable and Configure

Review the REST service definition in the REST API guides to leverage (available from the Oracle Help Center > *your apps service area of interest* > APIs & Schema). If you are new to Oracle's REST services you may want to begin with the Quick Start section.

To use this REST API, you must create a role and assign it to users with the required permission groups and associated security views.

Required permission groups:

Read: Revenue Source Document Additional Subline

  Create: Revenue Source Document Additional Subline

  Read: Revenue Source Document Line

  Read: Revenue Source Document

  Read: Revenue Pricing Line

To configure access:

Navigate to Security Console and create a new role.

  Enter a role name and enable Permission Groups.

  Add the required permission groups listed above.

  For each permission group, assign the All Rows, All Fields security view.

  Assign the role to the appropriate user.

## 💡 Tips and Considerations

• If any of the required attributes for processing are missing or invalid, a validation error is displayed with required corrective action.
• The API rejects the additional subline if the referenced source document line isn’t in processed status.
• The unique identifiers for both the source document line and the additional satisfaction event must be valid in order to successfully process and release the hold.
• Required values for satisfied quantity, satisfied percent, or amount applied depend on the event type and satisfaction measurement model.

## 🔐 Access Requirements

No new access requirements.

## 📚 Key Resources

• Additional Satisfaction Event Rules
• Revenue Recognition for Additional Satisfaction Events
• Guidelines for Importing Additional Satisfaction Events
• Guidelines for Working with Additional Satisfaction Events

---
*Oracle Cloud Readiness · 26C · ERP · Financials*