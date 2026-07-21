[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Oracle Fusion Field Service](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/oracle-fusion-field-service.md)

# Use Fusion Service Work Order Fields in Forms and Expanded Address Fields on Standard Screens

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/fscv-26c/26C-fsvc-wn-f49499.htm)

Oracle Fusion Service and Oracle Fusion Field Service already support a native end-to-end flow that connects service request management with field enablement. This allows Service Work Order information from Oracle Fusion Service to flow directly into Oracle Fusion Field Service, offering a more consistent data model and a simpler way to share work order information across service and field teams.

**Note**

  This enhancement only applies to Oracle Fusion Field Service environments. You can verify whether you've Oracle Field Service or Oracle Fusion Field Service, by signing in and checking on the **About** page.

The business value is a more connected service experience: contact center and service teams can manage the customer issue in Fusion Service, while dispatchers and field teams can use the related work order details in Fusion Field Service to plan, schedule, dispatch, and complete the work more efficiently.

Starting from 26C, Oracle is enhancing this existing native flow by adding more Service Work Order details, including additional address information on supported Field Service pages and support for Service Work Order fields in Field Service forms. This gives field teams better access to the information they need while continuing to support a consistent, native flow between Oracle Fusion Service and Oracle Fusion Field Service.

**Expanded Service Work Order Address Details on Field Service Screens**

Administrators can use additional Service Work Order address fields on supported Field Service screens. This is useful when a Service Work Order includes address details that help users identify the exact service location, such as a building and floor number. Instead of creating custom properties to show these details in Oracle Fusion Field Service, administrators can add the supported Service Work Order fields directly to the required pages.

The fields can be added to these activity-related pages:

• Activity Details
• Activity Hint
• Delay Activity
• Start Activity
• Suspend Activity
• Cancel Activity
• Complete Activity
• Not Done Activity

**Supported Service Work Order Address Fields**

  Administrators can add the following read-only Service Work Order address fields to supported Oracle Field Service pages.

Table: Supported Service Work Order Address Fields

Work Order Field | Field Label | Fusion Field Service UI Access
Building | Building | Read-only
County | Country | Read-only
Floor Number | FloorNumber | Read-only
Address Lines Phonetic | AddressLinesPhonetic | Read-only
Postal Code Extension | PostalPlus4Code | Read-only
Additional address element 1 | AddrElementAttribute1 | Read-only
Additional address element 2 | AddrElementAttribute2 | Read-only
Additional address element 3 | AddrElementAttribute3 | Read-only
Additional address element 4 | AddrElementAttribute4 | Read-only
Additional address element 5 | AddrElementAttribute5 | Read-only

**Formatted Address Field**

In this same update, Oracle Fusion Field Service introduces the formatted Address field for supported Oracle Field Service pages. The field uses the label formatted_address and displays the activity address as one formatted value. For Oracle Fusion Field Service, the formatted address follows the country-specific address format configured in Fusion Applications. If no address format is available for the applicable country, the default Oracle Field Service address order is used: street address, city, state, postal code, and country.

For example, for  a repair activity at a multi-building customer site, administrators can use Service Work Order address details such as **Building** and **Floor Number** in Oracle Fusion Field Service so the field resource can confirm the exact service location. They can show these details as separate fields on supported screens or as part of the formatted Address field, labeled formatted_address, when the address should follow the Fusion Applications country-specific address format.

See the related Formatted Address Field for Field Service Pages for complete setup and behavior details.

**Service Work Order Fields in Field Service Forms**

Administrators can also use Fusion Service Work Order fields in Oracle Fusion Field Service forms. This lets implementation teams include work order context in forms used by mobile workers during an activity. Most standard Service Work Order fields are read-only in Oracle Field Service forms. The **Field Service Note** and supported Service Work Order descriptive flexfields, also known as DFFs, can be updated from Oracle Field Service.

The following Service Work Order fields are supported in Oracle Field Service forms:

Table: Service Work Order Fields

Work Order Fields | Field Service UI Access
Work Order ID | Read-only
Reference Number | Read-only
Title | Read-only
Status | Read-only
Case Note | Read-only
Field Service Note | Read-write
Account Name | Read-only
Contact: Name | Read-only
Contact: Phone | Read-only
Contact: Alt Phone | Read-only
Contact: Email | Read-only
Address Line 1 | Read-only
Address Line 2 | Read-only
Address Line 3 | Read-only
Address Line 4 | Read-only
City | Read-only
Postal Code | Read-only
State | Read-only
Province | Read-only
Country | Read-only
Resolution Due Date | Read-only
Asset Serial Number | Read-only
Asset Name | Read-only

**Descriptive Flexfields (DFFs)**

The following DFF types are fully supported and configurable as **read-write**:

• Text
• Number
• Percentage
• Date
• Datetime
• Checkbox
• Fixed Choice

## 🎯 Business Benefit

This enhancement strengthens the native Oracle Fusion Service and Oracle Fusion Field Service flow by giving field teams more complete Service Work Order context in Oracle Field Service, while supporting a more consistent data model across service and field enablement.

Key benefits include:

• Supports guided field execution by displaying relevant Fusion Service Work Order information directly in Field Service forms.
• Improves field data capture by allowing field resources to update Field Service Notes and supported Service Work Order DFFs from Field Service forms.
• Reduces duplicate configuration by allowing customers to use native Service Work Order fields and DFFs in forms instead of creating separate Field Service properties for the same information.
• Improves location accuracy and usability by showing expanded Service Work Order address details and formatted address information on supported Field Service pages.

## ⚙️ Steps to Enable and Configure

Make sure activities are associated with their Service Work Orders. When the activity and Work Order are created, set the **Work Order ID** at the activity level. This can be done using APIs, if not using the native capability.

To add the Service Work Order fields to a Fusion Field Service page:

1. Go to **Configuration > Screens**.
2. Open the activity-related page where you want to show the Service Work Order address field.
3. Add the required Service Work Order address fields.
4. Save the page configuration.
5. Open an activity linked to a Service Work Order and verify that the fields appear as expected.

To add the Service Work Order fields to a Fusion Field Service form:

1. Go to **Configuration > Forms & Plugins**.
2. Create a form or open an existing form.
3. Add the needed Fusion Service Work Order fields or descriptive flexfields to the form.
4. Publish the form.
5. Open an activity linked to a Service Work Order and verify that the fields appear as expected.

## 💡 Tips and Considerations

• These Service Work Order address fields are read-only in Fusion Field Service.
• The activity must include the Work Order ID for Fusion Field Service to show values from the related Service Work Order.
• To show the full address in one formatted field, see the related 26C enhancement Formatted Address Field for Field Service pages.

## 📚 Key Resources

• Unified Oracle Fusion Field Service and Oracle Fusion Service Flows
• Related 26C enhancement: **Formatted Address Field for Field Service Screens**

---
*Oracle Cloud Readiness · 26C · SERVICE · Oracle Fusion Field Service*