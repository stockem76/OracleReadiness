[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# Enable Req Att Validation For REST API

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f46278.htm)

This Optional Feature, when enabled, validates the JSON payload for POST requests that create objects. The validation verifies that the required attributes needed to create the object are included in the payload. Any required attribute that does not have a default value in the database must always be included.  For the initial release - only the Order Release and Shipment resources have the required attribute and validation logic enhancement.  For the initial release, this Optional Feature only pertains to the Order Release and Shipment resources, but as addition resources are added, this Optional Feature will support Opt In and Opt Out for all of the required attribute enabled resources.

For more information see the 26C feature Required Attribute Validation for REST Resource Creation and Updates.

**Business Benefit:**This feature is provided as a way to, during the optional feature period, decide when to Opt In or Opt Out of the Required Attribute Validation for REST Resource Creation and Updates logic.  This feature is provided to support backward compatibility and avoid regression issues.  We recommend enabling the Optional Feature to gauge the impact of the new attribute validation logic on your integrations.

## ⚙️ Steps to Enable and Configure

If you need to change the Opt In state for this feature:

• Go to the Optional Feature UI - **Configuration and Administration > Property Management > Optional Features**.

Your user must have the DBA.ADMIN user role to use this functionality.

• Select the **Enable req att validation for rest api**feature.
• Run the desired Action for the feature - Opt In or Opt Out.

We recommend the following steps when introducing the new attribute validation functionality into your integration flows.

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

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*