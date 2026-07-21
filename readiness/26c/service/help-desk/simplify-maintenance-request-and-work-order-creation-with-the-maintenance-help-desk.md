[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Help Desk](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/help-desk.md)

# Simplify maintenance request and work order creation with the Maintenance Help Desk

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/shde-26c/26C-helpdesk-wn-f47354.htm)

There are new features that are now a part of the Maintenance Help Desk, whereby an employee can create a maintenance help desk request, and the maintenance manager can then create a work order, if necessary. New enhancements include:

• Filtering assets based on the operating organization (location) of the asset based on the default operating organization listed in a profile option
• Navigating to either Classic or Redwood Work Order pages based on a profile option
• Copying attachments to work orders
• Showing the work order link from the help desk request for the help desk agent (a.k.a. maintenance manager)
• The ability to create multiple work orders for a single maintenance request
• The ability to delete a work order association to a maintenance request and have the maintenance work order end dated
• Showing the asset number and description plus the organization name as reference when creating a maintenance work order
• Defaulting the Work Order Type to *Corrective*, and Work Order subtype to *Reactive* and defaulting the start date to the current time
• Making the Maintenance Operating Organization defaulted, but selectable if maintenance is to occur at a different operating organization location

This feature streamlines the end-to-end process for turning a maintenance-related Help Desk request into a maintenance work order by allowing employees to more easily find the asset that requires maintenance and reducing duplicate data entry.

## ⚙️ Steps to Enable and Configure

**Enable Default Operating Organization**

Most of the enhancements for the maintenance help desk are included by default. However, if you wish to default the asset operating organization for work requests, you may set ORA_MNT_ISR_DEFAULT_ASSET_ORG profile option. This should be done at the site level for everyone. For those having multiple operating organizations, you may wish to add entries at the user-level for those users who may not be associated with the primary location. To do this:

1. Go to **Setup and Maintenance**.
2. Click on the **Tasks** icon.
3. Click **Search**.
4. Search for **Manage Administrator Profile Values**, and click the resulting link.
5. Enter **ORA_MNT_ISR_DEFAULT_ASSET_ORG** in the Profile Option Code and Search.
6. Set a Site default value.
7. For persons affiliated with an operating organization that is not the default value, add a line for each employee with their operating organization selected.

**Configure links to Maintenance in the Redwood Experience**

If you want the Help Desk links to associated maintenance pages to open the Redwood version, you will need to enable the applicable Maintenance profile options to use the Redwood pages:

1. Go to **Setup and Maintenance**.
2. Click on the **Tasks** icon.
3. Click **Search**.
4. Search for **Manage Administrator Profile Values**, and click the resulting link.
5. Enter the following Profile Options and set the appropriate values for the desired functionality

• Maintenance Work Orders: ORA_MNT_SUPERVISION_REDWOOD_ENABLED
• Asset Details: ORA_MNT_ASSET_DETAILS_REDWOOD_ENABLED

### Pre-requisites

In order to take advantage of these new features, it is assumed that:

• You have already Set Up Maintenance, and that maintenance managers are able to create maintenance work orders for existing assets.
• Internal Service Request Help Desk is enabled and configured to allow for Maintenance requests to be created.

If Help Desk is not configured, you will need to enable the Maintenance Help Desk using the instructions below.

**Enable Maintenance Help Desk**

1. Go to **Setup and Maintenance**.
2. Click on the **Tasks** icon.
3. Click **Search**.
4. Search for **Manage Administrator Profile Values**, and click the resulting link.
5. Enter **SVC_NG_ENABLE_MAINTENANCE_HELPDESK** as the Profile Option Code and Search. 
  • If the profile option doesn't exist, click Cancel.
• Search for **Manage Profile Options** and click the resulting link.
• Create a profile option with this code: SVC_NG_ENABLE_MAINTENANCE_HELPDESK.
• Go to **Manage Profile Categories**.
• Search for the ORA_FND_AUTH_REST_ACCESS profile category.
• Add the SVC_NG_ENABLE_MAINTENANCE_HELPDESK profile option to the category.
• Return to the Manage Administrator Profile Values screen, and restart with Step 4.
6. Set the profile value to Y.
7. Save and close.

###

## 💡 Tips and Considerations

• The operating organization isn't saved on the Help Desk request if the request is saved without selecting an installed base asset.
• If your environment uses Redwood Maintenance pages, validate the work order and asset navigation profile options before rolling out the feature to users.
• Test the flow with users who have both Help Desk access and Maintenance access so you can confirm that cross-application navigation opens the correct pages.
• When a user removes the work order association from a Help Desk request, the integration sends an association end date to the maintenance work order.
• Use reporting or telemetry to monitor how many maintenance Help Desk requests are created and how many are converted into work orders.

Navigation to the Redwood version of the Work Order page is not working for the pre-release (SOAK) version, but it is planned to be available by the time the release is available in production.

To associate your maintenance manager to the Organizations they will manage:

1. Setup and Maintenance -> Manufacturing and Supply Chain Materials Management
2. Go to Maintenance Management
3. Click on Manage Inventory Organization Data Access for Users
4. Click on the radio button Users with Data Access
5. Add the user name and add the Role Maintenance Manager and click Search.
6. In the pop-up, add Row, and add the User Name, Role as Maintenance Manager, Security Context = Inventory Organization, and enter the Organization to which this maintenance manager belongs. You may click duplicate in the popup to add as many rows as needed to add associations to as many inventory orgs as necessary.

## 🔐 Access Requirements

No new privileges are required. However, if you are implementing a maintenance help desk for the first time, the following roles are recommended minimally, for the users of Help Desk:

To have access to Supply Chain Execution, you should have one or more of the following:

• Supply Chain Application Administrator - All Inv Orgs
• Supply Chain Application Administrator - All Cost Orgs
• Supply Chain Application Administrator - All Sets

All Employees:

• Employee
• Internal Help Desk User

Maintenance Managers (Determines whether a new maintenance work order is required or not):

• Employee
• Resource
• Internal Help Desk Agent
• Maintenance Manager (ORA_MNT_MAINTENANCE_MANAGER_JOB)

Maintenance Technician (The one doing the work and will need access to the maintenance request as well as the ):

• Employee
• Resource
• Internal Help Desk Agent
• Maintenance Technician (ORA_MNT_MAINTENANCE_TECHNICIAN_JOB)

Note that you may need to run "Import User and Role Application Security Data" as a scheduled job after adding all appropriate roles.

The delivered job roles outlined above provide the required Maintenance access for the asset and work order pages and Help Desk for submitting maintenance requests. If users are assigned delivered Help Desk and Maintenance roles that haven't been customized, the required access is available out of the box. If your organization uses custom roles, review those roles and add equivalent access.

## 📚 Key Resources

Documentation on how to set up your Maintenance Organization is found here: Set Up Maintenance

A video demonstrating this functionality can be found as part of the "What's New for Help Desk in 26C" Cloud Customer Connect Event on August 19, 2026.

After this feature is generally available, a video showing how to configure your environment and a demonstration of the functionality will be found on Oracle Video Hub: Fusion Help Desk.

---
*Oracle Cloud Readiness · 26C · SERVICE · Help Desk*