[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [HCM Common](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/hcm-common.md)

# AI Agent: Spreadsheet Data Loader Advisor for HSDL

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hcom26c/26C-hcm-common-wn-f49881.htm)

Oracle Fusion Cloud HCM introduces a new AI-powered Spreadsheet Data Loader (HSDL) Advisor that simplifies spreadsheet-based data loading through a guided conversational experience.

The HSDL Advisor enables you to upload CSV files and use natural language instructions to initiate HSDL processing. The advisor assists throughout the upload lifecycle, including business object identification, template discovery, column mapping, validation, file preparation, and data loading.

You can also interact with the advisor to receive guidance and insights related to HSDL data sets, templates, uploads, and supporting documentation using natural language questions.

**Salient Features:**

• Feature | Description
CSV-Based HSDL Upload Initiation | Users can upload a CSV file through the HSDL Advisor experience and optionally provide an active template code to initiate Spreadsheet Data Loader processing.
Automatic Business Object Identification | The advisor analyzes uploaded CSV headers to automatically identify the associated HSDL business object.
Active Template Discovery | After identifying the business object, the advisor displays all active spreadsheet templates available to the user for that business object.
Cross-Platform CSV Upload Support | CSV-based uploads are supported without requiring the Windows-only Desktop Integration tooling previously used for spreadsheet uploads, enabling HSDL uploads from platforms such as macOS.
Template Validation and File Preparation | The advisor validates the selected template, maps uploaded CSV headers to the template structure, and prepares the file before initiating the Spreadsheet Data Loader process.
Automated File Upload and Load Initiation | The processed file is uploaded to Oracle WebCenter, and the Spreadsheet Data Loader process is initiated automatically.
Load Progress Monitoring | The advisor provides a direct link to the Recent Spreadsheet Loads page where users can monitor load progress and processing results.
Conversational Guidance and Documentation Assistance | Users can interact with the advisor using natural language questions to receive guidance related to HSDL supporting documentation, setup, and configuration information.

**ACCESSING THE SPREADSHEET DATA LOADER ADVISOR -**

1. Navigate to **Navigator** > **Tools** > **AI Agent Studio**.
2. Open the **Agent Teams** tab.
3. In the **Product** filter, select **Data Loader**.
4. From the **Published** tab, locate **Spreadsheet Data Loader Advisor** and click the **View** icon to review the agent team configuration.
5. Click on the **View**icon under the **Actions**column to launch the **Spreadsheet Data Loader Advisor.**
6. Click on the **Play**icon to open the **Spreadsheet Data Loader Advisor**drawer.

**INITIATING AN HSDL LOAD**

Begin by uploading a CSV file and, optionally, provide the applicable active template code to initiate processing.

The HSDL Advisor automatically identifies the appropriate business object from the uploaded CSV file based on the column headers and displays all active templates associated with that business object. You can review the available templates and select the appropriate one using the **Approve** or **Request Change** options.

After template selection, the advisor validates the template availability and analyzes the uploaded column headers and file structure. It then maps and reorganizes the columns to align with the selected HSDL template format, uploads the transformed file to Oracle WebCenter, and automatically initiates the Spreadsheet Data Loader process.

The HSDL Advisor provides a direct link to the **Recent Spreadsheet Loads** page, allowing users to monitor upload and processing progress in real time.

You can also interact with the advisor to receive guidance and insights related to HSDL supporting documentation, setup, and configuration information.

• How do I install the HSDL extension for generating spreadsheets?
• Which template should I use for loading new hires?
• What active templates are available for the Worker business object?

**Business Benefit:**The HSDL Advisor agent significantly improves the spreadsheet data loading experience by reducing technical complexity, minimizing upload errors, and accelerating data preparation and execution. The enhancement helps in streamlining HCM data loading processes while improving usability, efficiency, and accuracy across spreadsheet-driven data management activities.

## ⚙️ Steps to Enable and Configure

For the document tools included in the **Spreadsheet Data Loader Advisor**you need to run the **Process Agent Documents** process to ingest the documents.

**Prepare the HCM*****Spreadsheet*****Data Loader AI Agent**

Before using the HSDL Advisor, run the required scheduled processes to prepare and index the agent documents used for document-based interactions.

1. Navigate to **Tools** > **Scheduled Processes**.
2. Click **Schedule New Process**.
3. Search for and select **Prepare the HCM*****Spreadsheet*****Data Loader AI Agent**
4. Click **OK**, and then select **Submit** to run the process.
5. After the process completes successfully, click **Schedule New Process** again.
6. Search for and select **Process Agent Documents**.
7. Click **OK**, and then select **Submit** to process and prepare the agent documents for use by the HSDL Advisor.

You need to perform the following steps to enable the HDL Agent in the HDL pages:

1. Enable the following profiles in the **Manage Administrator Profile Values** task in Setup and Maintenance:

• ORA_PER_GUIDED_JOURNEYS_ENABLED
• ORA_PER_GUIDED_JOURNEYS_SETUP_REDWOOD_ENABLED
• ORA_ASE_SAS_INTEGRATION_ENABLED
• ORA_HCM_VBCS_PWA_ENABLED

2. Configure the AI Advisor Guided Journey

• Navigate to **My Client Groups** and select **Show More**.
• In the **Journeys Setup** section, search for and open the **Guided Journey** quick action.
• Click **Create** to create a new Guided Journey.
• Enter a name for the Guided Journey and select **Create Draft**.
• Under the **Tasks** section, click **Add** and enter the required task details for the AI Advisor configuration.
• • Task Name | Name that appears in the guided journey banner at the top of the page. HCM Spreadsheet Data Loader AI Agent
Task Description | An optional description that appears below the task name in the guided journey banner. Upload csv files and initiate HSDL
Task Type | Agent
Agent Type | Workflow Agent
Workflow Agent | HCM Spreadsheet Data Loader Advisor
• Make a note of the generated **Guided Journey Code** and **Guided Journey Task Code** for use during page configuration in Visual Builder Studio.
• Click **Save**to enable the Guided Journey.

3. Extend the Run Spreadsheet Data Loader Page with the AI Advisor Guided Journey

• Navigate to the Run Spreadsheet Data Loade task from the **Data Exchange** work area.
• From the **Settings and Actions** menu in the global header, select **Edit Page in Visual Builder Studio**.

• Create a new **Visual Builder Studio** project or select an existing project.
• Configure the page properties by entering the **Guided Journey Code** and **Guided Journey Task Code** generated during **Guided Journey** setup into the following properties: 
  • guidedJourneyCode
• guidedJourneyTaskCodes
• Click **Preview** to validate and test interactions with the AI Advisor.
• Publish the page customizations according to your organization’s deployment and change management procedures.

Your environment must have the appropriate services for Oracle Applications Platform deployed. For more information, see FAQ2521 on My Oracle Cloud Support.
Set the Enable Security Console External Application Integration (ORA_ASE_SAS_INTEGRATION_ENABLED) profile option to Yes and enable permission groups for the appropriate roles. See Access Requirements for AI Agent Studio.

## 🔐 Access Requirements

SAS Roles and policy:

Display Name | Name | Description
Access HCM Spreadsheet Data Loader Advisor | ORA_DR_HRC_ACCESS_HSDL_LOADER_ADVISOR | Allows the user to access the HCM Spreadsheet Data Loader Advisor agent team.
Access Spreadsheet Data Loader Advisor Agent Team Policy | ORA_DR_HRC_ACCESS_HSDL_LOADER_ADVISOR_read | Allows users to access the HCM Spreadsheet Data Loader Advisor agent team

## 📚 Key Resources

• Explore AI Agents for Oracle Fusion Cloud Applications
• How do I use AI Agent Studio?

---
*Oracle Cloud Readiness · 26C · HCM · HCM Common*