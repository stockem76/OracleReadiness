[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Streamline the Import and Export of Messaging Setup Data

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f46531.htm)

You can now export and import Oracle Collaboration Messaging setup data to migrate your configuration across pods and environments like development, test, and production. Setup data includes messaging providers, connections, and partner configurations for both suppliers and customers.

You now have:

• **Faster environment provisioning:**Quickly replicate a known good configuration from one pod to another without rebuilding setups manually.
• **Reduced manual effort and fewer errors:**Eliminate repetitive data entry and lower the risk of misconfiguration.

## ⚙️ Steps to Enable and Configure

After you enable the **Simplify Configuration and Processing for B2B Messaging** feature, perform the following high-level tasks:

1. Create an implementation project.
2. Create a configuration package.
3. Export setup data.
4. Upload a configuration package.

**Create an Implementation Project**

1. From the Setup and Maintenance work area, click the **Tasks** icon and select **Manage Implementation Projects**.
2. Select **Create**.
3. Enter the required details, then select**Save and Open Project**.

Create Implementation Project

1. On the newly created implementation project, **Select**and **Add**.
2. In the search fields, enter:

• Search = Tasks
• Name = Manage Simplified Collaboration Messaging Configuration

1. Select **Apply**.

Select and Add Tasks

1. In the search fields, enter:

• Search = Tasks
• Name = Manage Collaboration Messaging Service Providers

1. Select **Apply**and **Done**.
2. On the Implementation Project page, select **Done**.

Implementation Project

**Create a Configuration Package**

1. From the Setup and Maintenance work area, click the **Tasks** icon and select **Manage Configuration Packages**.
2. Select **Create**.
3. In the **Name** field, select the implementation project that was previously created and select **Yes** in the warning dialog.
4. Enter the required details. Select **Save and Close**.

Create Configuration Package

**Export Setup Data**

1. On the Manage Configuration Packages page, select the package you just created, then select **Export Setup Data**.
2. On the Export Setup Data page, select **Submit**.

Export Setup Data

1. On the Manage Configuration Packages page, the status shows **Completed Successfully** when the export finishes without errors.

Manage Configuration Packages – Export Status

1. Download the configuration package by clicking **Download > Download Configuration Package**.

Download Configuration Package

**Upload a Configuration Package**

1. On the destination pod where the data will be imported, go to the **Setup and Maintenance** work area. Select the **Tasks** icon, select **Manage Configuration Packages**and **Upload**.

Manage Configuration Packages - Upload

1. Browse for the configuration package .zip file, and select **Get Details** and **Submit**.

Upload Configuration Package Details

1. On the Manage Configuration Packages page, the status shows **Completed Successfully** when the upload finishes without errors.

Manage Configuration Packages – Upload Successful

1. Select **Import Setup Data**.
2. On the Import Setup Data page, select **Submit**.

Import Setup Data – Submit

1. On to the Manage Configuration Packages page, the status shows **Completed Successfully** when the import finishes without errors.

Manage Configuration Packages – Import Successful

## 💡 Tips and Considerations

• To migrate the Collaboration Messaging configuration data of all the objects, you need to add:
• • Manage Simplified Collaboration Message Configuration
• Manage Collaboration Messaging Service Providers
• Any errors that get detected during the data export, upload, or import will be reported on the Export and Import Process Results page.

## 🔐 Access Requirements

You can work with Functional Setup Manager (FSM) if you have the Application Implementation Consultant role.

## 📚 Key Resources

For more information, refer to these resources on the Oracle Help Center.

Setup Data Export and Import chapter of the Using Functional Setup Manager guide.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*