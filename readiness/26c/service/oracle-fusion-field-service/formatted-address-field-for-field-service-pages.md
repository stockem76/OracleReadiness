[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Oracle Fusion Field Service](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/oracle-fusion-field-service.md)

# Formatted Address Field for Field Service Pages

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/fscv-26c/26C-fsvc-wn-f49558.htm)

In Update 26C, administrators can add a new **Address** field to supported Field Service pages. The field uses the label formatted_address and displays the address as one formatted value instead of requiring users to review each address component separately.

This is useful when the activity pages include several individual address fields, or when mobile users need a compact view of the location before starting work. By adding the **Address** field, administrators can show the full activity address in one place while keeping the page layout easier to read.

The **Address** field can be added to these activity-related pages:

• Activity Details
• Activity Hint
• Delay Activity
• Start Activity
• Suspend Activity
• Cancel Activity
• Complete Activity
• Not Done Activity

**Behavior of the Address Field**

The behavior of the **Address** field depends on the Fusion Field Service subscription being used.

**Oracle Field Service:**The field uses the default Field Service address order. The formatted address is built from the available activity address components in this order: street address, city, state, postal code, and country. This order is similar to a common United States address presentation.

Oracle Field Service default address order example:

500 Oracle Parkway

  Redwood City, CA 94065

  United States

**Oracle Fusion Field Service:**The field follows the country-specific address format configured in Fusion Applications. Administrators manage these formats in the **Setup and Maintenance** work area using the **Manage Address Formats** task.  This allows the address to follow the format defined for the applicable country. If no address format is defined in Fusion Applications for the applicable country, Oracle Fusion Field Service uses the default Field Service address order.

Different countries can use different address structures. In France, addresses commonly show the postal code before the city.

Oracle Fusion Field Service country-specific format example:

10 Rue de la Paix

  75002 Paris

  France

  For Oracle Fusion Field Service, the actual order and included address elements depend on the address format configured in Fusion Applications for the country.

The **Address** field with the label formatted_address is available to add to supported Fusion Field Service pages. It is not available for customer API operations.

## 🎯 Business Benefit

• Improve readability by showing the full address in one formatted field.
• Reduce page clutter by allowing administrators to use one formatted address field instead of several individual address fields.
• Help dispatchers and field resources read location details faster from activity pages.
• Support country-specific address presentation for Oracle Fusion Field Service customers using Fusion Applications address formats.

## ⚙️ Steps to Enable and Configure

The **Address** field is available automatically in Update 26C.

For Oracle Fusion Field Service, review the address format setup in Fusion Applications:

1. Go to the **Setup and Maintenance** work area.
2. Select the **Customer Data Management** offering.
3. Open the **Trading Community Foundation** functional area.
4. Open the **Manage Address Formats** task.
5. Review the address format for the required country.
6. Return to **Fusion** **Field Service** and verify the formatted address on the configured page.

To add the formatted address to a page:

1. Go to **Configuration** > **Screens**.
2. Open the activity-related page where you want to show the formatted address.
3. Add the **Address** field.
4. Confirm that the field label is formatted_address.
5. Save the page configuration.
6. Open an activity with address information and verify that the formatted address appears as expected.

## 💡 Tips and Considerations

• Oracle Field Service uses the default Field Service address order: street address, city, state, postal code, and country.
• Oracle Fusion Field Service uses the country-specific address format configured in Fusion Applications. If no address format is defined in Fusion Applications for the applicable country, Oracle Fusion Field Service uses the default Field Service address order.

---
*Oracle Cloud Readiness · 26C · SERVICE · Oracle Fusion Field Service*