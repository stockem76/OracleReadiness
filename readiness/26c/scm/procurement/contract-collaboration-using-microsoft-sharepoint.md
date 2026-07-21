[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Procurement](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/procurement.md)

# Contract Collaboration using Microsoft SharePoint

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/proc26c/26C-procurement-wn-f47272.htm)

You can now collaborate on contract terms using Microsoft SharePoint from the Microsoft Word Add-in. This feature lets contract managers, legal users, and internal stakeholders review and update a shared contract terms document in SharePoint instead of exchanging multiple document copies over email.

When collaboration is started, the contract terms document is uploaded to the configured SharePoint site. A contract-specific folder is created in SharePoint, and the contract terms file is placed in that folder. The SharePoint-hosted document becomes the working copy for collaboration, allowing users to review, comment, and edit the same file based on their assigned access. This improves collaboration by helping teams work from a single shared document, reducing version conflicts, avoiding manual consolidation of feedback, and improving visibility into comments and changes.

**Key Features**

With Microsoft SharePoint contract collaboration, contract managers, legal users, and internal stakeholders can work together on a shared contract terms document from the Microsoft Word Add-in.

This capability includes:

• **SharePoint-based collaboration for contract terms**: Start collaboration from the Word Add-in and work on a shared contract terms document in Microsoft SharePoint.
• **Automatic SharePoint folder and file setup**: When collaboration starts, the application programatically creates a contract-specific folder in the configured SharePoint site and stores the contract terms file in that folder.
• **Single shared working copy**: The SharePoint-hosted document becomes the working copy for collaboration, helping users avoid multiple local copies and email-based document exchanges.
• **Contract contacts as collaborators**: Internal contract contacts are included as collaborators, with SharePoint access defaulted from their contract access.
• **Independent SharePoint access control**: The collaboration initiator can update each collaborator’s SharePoint access, such as **Can edit**, **Can view**, or **No access**. These changes apply only to the SharePoint folder or file and don’t change contract access in the application.
• **Microsoft Word collaboration tools**: Collaborators can use Microsoft Word capabilities such as coauthoring, comments, assigned tasks, reviewing, and tracked changes.
• **Email notifications for collaborators**: Collaborators can receive Microsoft notifications when they’re invited to access or review the shared folder or document.
• **Manage access during collaboration**: The collaboration initiator can manage collaborator access after the collaboration session has started.
• **Upload final terms back to the application**: When review is complete, the lock owner can leverage word add-in capabilities and upload the final reviewed contract terms back to the application.

**How It Works**

1. Open Microsoft Word and launch the Contracts Word Add-in.
2. Connect to the application 
  • Click on Connect to Login
3. Enter your Fusion application credentials 
  • Application login from Word Add-in
4. Download the contract terms 
  • From the Word Add-in, search for and download the contract terms for which you want to start collaboration. 
    • Download Terms from Add-in
5. Start collaboration from Microsoft Word - 
• Open the contract terms in Microsoft Word and use the Word Add-in to start collaboration. From the add-in, open the actions menu and select **Collaborate**.
• Click on Collaborate
6. A Microsoft sign-in window appears. Enter your Microsoft account credentials to continue 
  • Sign in to Microsoft
7. Review collaboration details
• The **Collaborate** drawer shows the SharePoint collaboration details, such as the collaboration platform, site, folder, file name, and collaborators. The listed collaborators are the internal contacts on the contract. Their SharePoint access is defaulted based on their contract access.
• Collaborate Drawer Details
8. Adjust collaborator access, if needed
• Before starting collaboration, the initiator can update each collaborator’s SharePoint access to **Can edit**, **Can view**, or **No access**. These changes apply only to the SharePoint collaboration location. They don’t change the user’s contract access in application.
• Collaborators Access Change
9. Start the collaboration session
• After reviewing the details and access, the initiator clicks **Collaborate**. The application opens the contract terms in Microsoft SharePoint. In the background, it creates the contract-specific folder in the configured SharePoint site and posts the contract terms file to that folder.
• Terms opening as SharePoint File
10. Collaborate on the shared document
• The SharePoint-hosted file becomes the working copy for collaboration. Collaborators work on the same contract terms document instead of exchanging separate copies over email. Users can use Microsoft Word capabilities such as comments, assigned tasks, coauthoring, and tracked changes to review and update the terms.
• SharePoint File
• Contract Terms Tab during Collaboration
• **Contract Terms Actions During Collaboration**
• When contract terms are in collaboration, the **Contract Terms** tab shows the collaboration status and the available actions for the contract terms document.
1. Unlock Terms
2. Edit in Microsoft Word
3. Upload Contract
4. Actions in Redwood during Collaboration
11. Notify collaborators
• Collaborators receive Microsoft notifications when they’re invited to access the shared folder or when they’re mentioned or assigned a task in the document. They can open the document from the notification and complete their review.
• Collaborators getting the email notification to collaborate
12. Review changes in one place
• Because everyone works on the same SharePoint-hosted document, comments, edits, and task updates are visible in one place. This helps the contract owner and reviewers validate updates without manually consolidating feedback from multiple files.
• Collaborator commenting to review a clause
• Email received to review the comments
• Collaborator reviewing and making the changes
• Initiator can verify the changes made
13. Manage access during collaboration
• After collaboration starts, the initiator can use **Manage Access** from the Word Add-in to review or update collaborator SharePoint access. Any changes made here continue to apply only to the SharePoint collaboration folder or file and don’t affect the users’ contract access.
• Manage Access Action
• Manage Access Details
14. Upload final terms
• When the review is complete, the lock owner uploads the final contract terms back to the application from the Word Add-in. This updates the contract terms in the application with the reviewed version.
• Uploaded Terms under Documents section

**Note:**When collaboration starts, the application automatically creates the required SharePoint folder and stores the contract terms file in the configured SharePoint site. If collaboration is initiated again for the same contract after uploading, the previous collaboration file is moved to an Archive folder for audit and reference, and the new contract terms file becomes the active working copy.

Folder Created in configured SharePoint Site

Terms posted in SharePoint Folder under the configured Site

Archive Folder for preserving past collaboration Files

Past Collaboration Files under Archive Folder

• **Faster contract reviews:** Stakeholders can review and update the same SharePoint-hosted contract terms file, reducing delays caused by sending files back and forth over email.
• **Fewer version conflicts:** Collaboration happens on a single shared working copy, so teams don’t need to manually compare or consolidate changes from multiple document versions.
• **Improved visibility and coordination:** Comments, edits, assigned tasks, and tracked changes are captured in one place, making it easier for reviewers to see the latest updates and respond quickly.

## ⚙️ Steps to Enable and Configure

**Step 1:**

**Configure the Microsoft Azure Application**

**Register the Application**

As an Azure administrator, sign in to the Microsoft Entra admin center: https://entra.microsoft.com/#home

1. On the home page, search for **App registrations**.
2. Click **App registrations**.
3. Click **New registration**. 
• Click on New Registration from App Registrations
4. On the **Register an application** page, enter a name for the application. 
• Enter Application Name
5. For **Supported account types**, make sure **Single tenant only - MSFT** is selected.
6. Skip **Redirect URI** for now.
7. Click **Register**.
8. After registration, you’re redirected to the **Overview** page.
9. Copy these values for later use: 
• **Application (client) ID**
• **Directory (tenant) ID**
• Overview Tab after Registration

**Add Redirect URIs**

The redirect URI is needed to redirect the Word Add-in to the appropriate page after the required details are fetched from the Microsoft response during sign-in.

1. In the navigation pane, click **Authentication (Preview)**.
2. Click **Add Redirect URI**. 
• Click on Add Redirect URI from Authentication (Preview)
3. On the **Configure platforms** page, click **Web**. 
• Click on Web
4. In the **Redirect URIs** section of the **Configure Web** window, add the required URI.
• Format: https://<host>/fscmUI/o365Contracts/web/msAuthCodeRedirect.html
• Configure Redirect URI
5. Click **Configure**.
6. Click **Cancel** on the drawer to return to the main page. 
• Click on Cancel
7. Click **Settings**. 
• Checkmark ID Tokens and Enable Allow Public client flows from Settings tab
8. Make sure **ID tokens (used for implicit and hybrid flows)** is selected.
9. **Allow public client flows** is enabled
10. Click **Save**.

**Specify Client Secret and Expiry**

1. In the navigation pane, click **Certificates & secrets**.
2. On the **Certificates & secrets** page, in the **Client secrets** section, click **New client secret**. 
• Go to Client Secrets from Certificates & Secrets
3. In the **Add a client secret** window, enter this description: Eg: Contract Addin client secret 
  • Click on New client secret and add description, expiry details
4. Select a duration for the client secret expiration. Recommended duration: 24 months
5. If you select **Custom**, enter the start and end dates. The dates must be within a 24-month time span.
6. Click **Add**.
7. Copy the generated string from the **Value** field. This is the **Client Secret Value**. Save it for later use.
• **Note:** Copy the client secret value immediately after it is generated. This value is visible only once. If you view it later, it appears as a masked entry and can’t be retrieved.
8. Copy the **Client Secret Expires** date. Save this date for later use.
• Copy and Save Expiry date and value

**Add API Permissions**

1. In the navigation pane, click **API permissions**.
2. Click **Add a permission**. 
• Click on Add a Permission from API Permissions
3. On the **Request API permissions** page, on the **Microsoft APIs** tab, select **Microsoft Graph**. 
• Click on Microsoft Graph
4. Click **Delegated permissions**. 
• Select Delegated Permissions
5. Add these permissions:

Permissions to be added

Permission | Description
openid | Sign users in
email | View users' email address
profile | View users' basic profile
Sites.ReadWrite.All | Edit or delete items in all site collections
Files.ReadWrite | Have full access to user files

Search and Add the required permissions

Remove User.read permission if it is added by default

1. Click **Add Permissions**. 
• Review the added permissions
2. On the **API permissions** page, in the **Configured permissions** section, click **Grant admin consent.**
• Click on Grant admin consent for MSFT
• Make sure the status for each permission is getting updated to Granted for MSFT

**Step 2:**

**Enable the Contract Collaboration Opt-in**

1. Go to **Setup and Maintenance**.
2. Click **Change Feature Opt In**. 
• Change Feature Opt-in
3. On the **Opt In** **: Enterprise Contracts** page, click the edit icon for **Enterprise Contracts**. 
• Enterprise Contracts Features
4. In the feature list, locate **Contract Collaboration**. 
• Checkmark Contract Collaboration Opt-in
5. Select the **Enable** check box for **Contract Collaboration**.
6. Click **Done**.

**Step 3:**

**Setup the Integration in Application Composer**

1. Sign in to the **Sales** application.
2. Navigate to **Configuration** > **Application Composer**.
3. Navigate to **Word Add-in Registration**. 
• Word Add-in Registration from Application Composer
4. Enter the values captured from the Azure Portal setup:
• Enter the values from Azure Portal Setup
Field | Value to Enter
Application (client) ID | Enter the Application Client ID copied from Azure.
Client Secret Value | Enter the client secret value generated in Azure.
Primary Microsoft Domain | Enter the primary Microsoft domain for the tenant.
Directory (tenant) ID | Enter the Directory Tenant ID copied from Azure.
Client Secret Expires | Enter the client secret expiration date copied from Azure.
Alternate Microsoft Domains | Optional and not needed for now.
Scope | openid email profile Sites.ReadWrite.All Files.ReadWrite
Microsoft Login Domain | https://login.microsoftonline.com
Primary SharePoint Domain | https://<Tenant-Name>.sharepoint.com Example: https://wftmh.sharepoint.com
5. Configuration in Application Composer
6. Save your changes.

**Step 4:**

**Create a SharePoint Site for Contract Collaboration**

Before you configure the SharePoint Site URL in Contracts application, create a Microsoft SharePoint site where contract terms files will be stored during collaboration.

1. Sign in to **Microsoft SharePoint** with an admin account that has permission to create sites. 
  • Microsoft SharePoint Login
2. On the SharePoint home page, click **Create**. 
  • Click on Create
3. In the **Create** panel, select **Site**. 
  • Select Site
4. On the **Create a site: Select the site type** page, select **Team site**. 
  • Select Team Site
5. On the **Select a template** page, select **Standard team**. 
  • Select Standard Team
6. On the **Preview and use ‘Standard team’ template** page, click **Use template**. 
  • Click on Use Template
7. On the **Give your site a name** page, enter the site details:
• **Site name**: Enter a name for the site, Eg: Contracts or Enterprise Contracts
• **Site description**: Optionally enter a description.
• **Group email address**: Optionally review or update the generated group email address.
• **Site address**: Optionally review or update the generated site address.
• Site Details
8. Click **Next**.
9. On the **Set language and other options** page, select the privacy and language options: 
  • **Privacy settings**: Select **Private - only members can access this site**.
• **Select a language**: Select the site language.
• Privacy and Language Settings
10. Click **Create site**.
11. On the **Add site owners and members** page, add site members only if required.
• You can skip adding members at this stage.
• Skip adding Members
12. Click **Finish**.
13. After the site is created, open the site 
  • SharePoint Site
14. Copy the site URL from the browser address bar. You’ll use this URL when configuring SharePoint Site URL in Enterprise Contracts application at Contract Type or Business Function Level.

**Step 5:**

**Configure SharePoint Collaboration Setup**

After you enable the **Contract Collaboration** opt-in, you can configure the Microsoft SharePoint site used for contract terms collaboration.

You can configure SharePoint collaboration at either of these levels:

• **Contract Type**
• **Business Function**

Contract Type setup takes precedence over Business Function setup. If a SharePoint site is configured for the contract type, that site is used. If it isn’t configured for the contract type, the application uses the SharePoint site configured for the applicable business unit and business function. If SharePoint isn’t configured at either level, users can’t start collaboration from the Word Add-in.

1. **Configure the SharePoint Site URL for a Contract Type**
1. Go to **Setup and Maintenance**.
2. In the **Search Tasks** field, search for **Manage Contract Types**. 
• Manage Contract Types Selection
3. Click **Manage Contract Types**.
4. Search for and select the contract type where you want to configure SharePoint collaboration.
5. In the **Contract Type Options** section, go to the **Advanced Authoring Options** tab.
6. Make sure **Enable terms authoring** is selected. 
• SharePoint URL at Contract Type level
7. In the **Collaboration Platform** field, select **Microsoft SharePoint**.
8. In the **SharePoint Site URL** field, enter the SharePoint site URL.  
    1. Example: https://your-company.sharepoint.com/sites/Site-Name
2. The SharePoint Site URL must:
• Start with https://
• Contain sharepoint.com t
• Use a valid SharePoint site format, such as: https://<tenant>.sharepoint.com/sites/<site-name>
• If the URL is missing or incorrectly formatted, the application displays a validation error.
9. Click **Save** or **Save and Close**.
2. **Configure SharePoint Collaboration for a Business Function**
1. Use this setup when you want SharePoint collaboration to apply to contracts for a specific business function.
2. You can configure the SharePoint site independently for:
• Customer Contracts
• Supplier Contracts
3. The SharePoint URL configured for Customer Contract Management Business Function isn’t reused for Supplier Contract Management Business Function, even when both are configured for the same business unit. Follow the below steps:
4. Go to **Setup and Maintenance**.
5. In the **Search Tasks** field, search for one of these tasks: 
    • **Specify Customer Contract Management Business Function Properties**
• **Specify Supplier Contract Management Business Function Properties**
6. Select the task for the business function that you want to configure.
7. Select the **Business Unit**. 
    • Business Function Task
8. In the **Collaboration** section, select **Microsoft SharePoint** from the **Collaboration Platform****dropdown**
9. In the **SharePoint Site URL** field, enter the SharePoint site URL.
• Example:
https://your-company.sharepoint.com/sites/Site-Name
• Configuring SharePoint URL at Business Function Level
10. Click **Save**.

**Step 6:**

**Create a Microsoft 365 Group in Microsoft Entra**

Create a Microsoft 365 group in Microsoft Entra and add the users who will participate in contract collaboration. This group is used later in the Power Automate flow to assign the required SharePoint permissions.

1. Go to the Microsoft Entra admin center: https://entra.microsoft.com
2. Sign in with an admin account that has permission to create groups.
• Entra Admin Center Home Page
3. In the left navigation pane, click **Groups**.
4. On the **Groups | Overview** page, click **New group**. 
  • Groups
5. On the **New Group** page, enter the group details 
  • New Group Creation Details
Field | Value
Group type | Select Microsoft 365 .
Group name | Enter a name for the group, such as CM Group
Group email address | System generated. Recommendation is to leave it as is.
Group description | Enter a description, such as Contract Collaboration group
Microsoft Entra roles can be assigned to the group | Select No .
Membership type | Select Assigned .
• Enter Group Creation Details
6. In the **Members** section, click **No members selected**.
7. In the **Add members** drawer, search for and select the users who will participate in contract collaboration. 
  • Add Members Drawer
8. Click **Select**.
9. Confirm that the selected members are listed in the **Members** section. 
  • Group Members Added
10. Click **Create**.
11. After the group is created, copy the group’s Object ID. You’ll need this value when running the Power Automate flow.
• In Microsoft Entra, go to **Groups** > **All groups**. 
    • Open the Group from All Groups
• Search for and select the group you created.
• On the group **Overview** page, copy the **Object ID**.
• Example: 96ecebe1-1084-4d2b-b51a-112fa4320d82
• Copy Object ID for future reference
• Save the Object ID. This is the value to enter as **EntraGroupID** when you run the Power Automate flow.

**Step 7:**

**Create a Power Automate Flow**

**Prerequisites**: Before running the Power Automate flow, complete these prerequisites: Create a Microsoft 365 group in entra.microsoft.com. The Microsoft 365 group should contain all users who will participate in contract collaboration. After you complete the prerequisites, follow these steps to create the Power Automate flow

1. Go to https://make.powerautomate.com/
2. Click on **My flows** option in the left toolbar.
3. Click on **Instant cloud flow** option in the New flow dropdown.
• Select Instant Cloud Flow from My Flows
4. Select **Manually trigger a flow** option and give a **Flow Name**.
• Choose manually Trigger a flow
• Enter Flow Name
5. In the Manually trigger a flow action, add two parameters(Click on Add an input button and select **Text** as the type of user input) :
1. SiteURL - Please enter the full SharePoint Site URL(format : https:abc.sharepoint.com/sites/Test)
2. EntraGroupID - Please enter the Entra Group ID
3. Add Parameters by Clicking on Add an input

Select Text
4. Add Parameters
6. Add a new action by clicking on the plus(+) icon - **Initialize variable**
• Initialize Variable
• Modify Initialize Variable
• 1. Rename action to **Initialize** **Sharepoint Site URL**
2. Enter **varSiteUrl** in the Name field - This is the variable which will be used to refer to the Sharepoint site in the subsequent actions.
3. Select Type as **string**.
4. In the Value field, click and select the top option **Dynamic Content**and pick **SiteURL**
5. Add Initialize SharePoint Site URL
7. Add a new action by clicking on the plus(+) icon - **Initialize variable**
1. Initialize Entra Group
2. Rename action to **Initialize Entra Group**.
3. Enter **varEntraGroupId** in the Name field - This is the Entra group's object id value which can be fetched by searching in entra.microsoft.com.
4. Select Type as **string**.
5. In the Value field, click and select the top option **Dynamic Content**(there will be another option Expression below Dynamic Content).
6. Enter Name Type and Value
7. Search for EntraGroupID
8. Select EntraGroupID as Value
9. EntraGroupId is added as the variable
8. Add a new action by clicking on the plus(+) icon - **Send an HTTP request to SharePoint**
1. Select Send and HTTP request to SharePoint Action
2. Rename the action to **Create Custom Role**.
• Create Custom Role
3. In the Site Address, click and select the option "Enter custom value" and then select the top option Dynamic Content - Select **varSiteUrl** from the window.
• Click on Enter Custom Value
• Search for VarSiteURL
• Select VarSiteURL as Site Address
4. Select Method as **POST** and enter the following in the Uri field – 
1. _api/web/roledefinitions
5. In the Advanced parameters option, select **Header** and add the following :
1. Accept : application/json;odata=nometadata
2. Content-Type: application/json;odata=nometadata
3. Add method Uri and Header parameters
6. In the Advanced parameters option, select **Body** and add the following :

{

"BasePermissions": {

"High": "1073742256",

"Low": "1044583151"

},

"Description": "Edit access plus Manage Permissions",

"Name": "Edit Plus Manage Permissions"

}

1. 1. Add body parameters
2. The values for High and Low are based on the custom role that we intend to create - Copy of Edit access level but with Manage Permissions option checked.
• Enter High and Low values
3. In the **setting** tab, under the **Retry policy** option, select **None**.
• Select None for Retry Policy Option under Settings Tab
2. Add a new action by clicking on the plus(+) icon - Delay
1. Select Delay as an Action
2. Enter **15** as **Count** and select **Second** in **Unit**
• Update the parameter values
3. In the **setting** tab, under the **Run After** option, **Create Custom Role** would be listed.
• Select Create Custom Role under Run After
4. Click on the three dots(...) listed next to it and select **Is successful, Has timed out** and **Has failed.**
• Select the required actions
3. Add a new action by clicking on the plus(+) icon - **Send an HTTP request to SharePoint**
1. Rename the action to **Create Custom Document Library.**
• Rename action to Create Custom Document Library
2. In the Site Address, click and select the option "Enter custom value" and then select the top option Dynamic Content - Select **varSiteUrl** from the window.
3. Select Method as **POST**and enter the following in the Uri field - _api/web/lists 
    • Update the Parameter details
4. 1. In the Advanced parameters option, select **Headers** and add the following :
• Accept : application/json;odata=nometadata
• Content-Type: application/json;odata=nometadata
• Header parameters
5. 1. In the Advanced parameters option, select **Body** and add the following :

{

"BaseTemplate": 101,

"Title": "Enterprise Contracts Collaboration"

}

1. 1. Body Details
2. In the **setting** tab, under the **Run After** option, **Delay** would be listed.
• Expand Delay under Settings Tab
3. Click on the three dots(...) listed next to it and select **Is successful**.
• Select Is Successful
4. In the **setting** tab, under the **Retry policy** option, select **None**.
• Select None under Retry Policy
2. Add a new action by clicking on the plus(+) icon - **Send an HTTP request to SharePoint**
1. Rename the action to **Ensure Group Exists**.
• Rename the action to Ensure Group Exists
2. In the Site Address, click and select the option "**Enter custom value**" and then select the top option Dynamic Content - Select **varSiteUrl** from the window.
• Search for Variables
• Select varSiteUrl
3. Select Method as **POST** and eneter the following in the Uri field -

_api/web/ensureuser

1. 1. In the Advanced parameters option, select **Header** and add the following :
1. Accept : application/json;odata=nometadata
2. Content-Type: application/json;odata=nometadata
3. Header Parameters
2. 1. In the Advanced parameters option, select **Body** and add the following :
• {"logonName":"c:0o.c|federateddirectoryclaimprovider|@{variables('varEntraGroupId')}"}
• Body Details
3. 1. In the **setting** tab, under the**Run After** option, **Create Custom Document Library** would be listed.
• Settings Tab
2. Click on the three dots(...) listed next to it and select **Is successful, Has timed out** and **Has failed**.
• Selection of Run After Settings
4. Add a new action by clicking on the plus(+) icon - **Send an HTTP request to SharePoint**
1. Rename the action to **Break Inheritance**.
• Rename action to Break Inheritance
2. In the Site Address, click and select the option "**Enter custom value**" and then select the top option Dynamic Content - Select **varSiteUrl** from the window.
• Search for Site Address
• Select varSiteURL
3. Select Method as **POST**and enter the following in the Uri field - 
• _api/web/lists/getbytitle('Enterprise Contracts Collaboration')/breakroleinheritance(copyRoleAssignments=false, clearSubscopes=true)
5. Add a new action by clicking on the plus(+) icon - **Send an HTTP request to SharePoint**
1. Rename the action to **Assign Custom Role.**
• Select Assign Custom Role
2. In the Site Address, click and select the option "**Enter custom value**" and then select the top option Dynamic Content - Select **varSiteUrl**from the window.
3. Select Method as **POST** and enter the following in the Uri field - 
• _api/web/lists/getbytitle('Enterprise Contracts Collaboration')/roleassignments/addroleassignment(principalid=@{outputs('Ensure_Group_Exists')?['body/Id']}, roledefid=@{outputs('Create_Custom_Role')?['body/Id']})
• Select varSiteURL and update Uri
6. Save the flow and run it manually by passing in the Sharepoint Site URL and Entra Group Id once prerequisites have been done.
• Sharepoint Site URL - Copy paste the Sharepoint URL
• Eg: https://<Tenant Name>.sharepoint.com/sites/Site Name
• `Entra Group ID - Copy paste the Object ID from Entra group you created. 
    • Updated Flow
• Run Flow using Run Option
• Flow Run Success Message
• Flow Status from Run History

---
*Oracle Cloud Readiness · 26C · SCM · Procurement*