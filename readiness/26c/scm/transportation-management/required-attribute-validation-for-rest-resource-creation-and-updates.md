[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# Required Attribute Validation for REST Resource Creation and Updates

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f47315.htm)

This feature introduces the concept of required attributes for an object.  For enabled objects, the list of defined required attributes for an object are validated in the initial steps of processing a JSON payload for the REST POST or PATCH (while creating new child resources) action.  Previously, integrations could fail later in processing due to missing data, often resulting in generic database or integrity constraint errors that were difficult to diagnose. With this enhancement, validation occurs earlier in the request lifecycle, helping you identify incomplete payloads before they trigger downstream processing issues.

For this initial release the required attributes and validation have been added to the Order Release and Shipment resources. In upcoming releases, the required attribute and validation logic will be added to all the supported resources.

This feature will improve the quality and reliability of REST API integrations by validating required attributes before a resource is created or updated. When you submit REST POST or PATCH requests for supported business objects, the application now checks whether mandatory fields are included and returns clearer, business-friendly validation messages when required information is missing.

**Business Benefit:** This feature helps you reduce REST integration failures by validating mandatory business data before transactions are processed.

Key benefits include:

• Reduced manual troubleshooting caused by incomplete payloads
• Faster issue resolution through clearer validation messages
• Improved data consistency across integrated systems
• Fewer downstream processing and database errors
• More reliable automation for shipment, order, invoice, and tender integrations

## ⚙️ Steps to Enable and Configure

We recommend the following steps for introducing the new attribute validation functionality into your integration flows.

1. Review the REST resources used by your integrations. 
  • Identify which business objects require mandatory attribute validation for your business processes.
2. Configure required attributes for supported resources. 
  • Required attributes are defined in the resource configuration definitions for each REST business object.
• Add the applicable attributes to the required attribute list for the resource.
3. Validate your integration payloads. 
  • Ensure your REST POST and PATCH requests include all required attributes for the target resource and nested child resources.
4. Test your integrations using representative business scenarios. 
  • Verify that successful requests include all mandatory values.
• Confirm that missing or null values return the expected validation message.
5. Deploy the updated configuration to your environments following your normal promotion and change management process.

## 💡 Tips and Considerations

• For this release the required attributes and validation has been added to the Order Release and Shipment resources. In upcoming releases, the required attribute and validation logic will be added to all the supported resources.
• Required attribute validation applies to both root-level resources and nested child resources included in REST payloads.
• PATCH operations now return improved validation messages when required attributes are missing or empty.
• Null or empty values for required attributes are validated and return business-friendly error messages instead of low-level database exceptions.
• Some attributes are intentionally excluded from validation because they are automatically generated or maintained by the application.
• Before enabling validation broadly, review your existing integrations carefully to avoid unexpected failures in legacy payloads that previously relied on implicit defaults or downstream validation.
• Start with high-volume transactional objects such as: 
  • Order Releases
• Shipments
• When validating nested resources, ensure all required child object attributes are included even if the parent object is valid.

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*