[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Project Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/project-management.md)

# Project Change Order Initiation Assistant

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/ppm26c/26C-ppm-wn-f49453.htm)

Leverage generative AI to create a change order from a project issue. For issues that need a change order, using the information available in the issue, the project manager can now create a change order effortlessly. With the ability to also extract and create detailed budget impacts automatically, the business process from when an issue is raised to creating a change order and then finally updating the project budget to reflect the new amounts can be performed with very minimal manual effort.

**Note:**Previously available in Prompt Lab, the 24D Change Order Generation from Project Issue feature is now migrated to Fusion AI Agent Studio.

These are the business benefits:

• Speeds issue resolution through change management, helping mitigate project risk and protect profitability.
• Reduces administrative effort in the change management process, allowing resources to be redirected to more strategic work.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Project Execution Management*

To access this feature, complete the following steps:

• Enable the **Change Order Generation from Project Issue** feature through FSM Opt In.
• Enable the required permission groups in Security Console for each role that will use this feature.

**To enable permission groups:**

1. Navigate to **Navigator > Tools > Security Console** and click **Roles**.
2. Search for the job role you want to use for the generative AI feature and select **Edit Role**.
3. On the Basic Information page, click **Enable Permission Groups**, and confirm your choice.
4. Open the Role Hierarchy step. If needed, go to the Roles and Permission Groups tab and add the required feature-specific duty role and any required runtime duty role.
5. Click **Summary**, then click **Save and Close**.

If your organization uses custom roles, add the appropriate feature-specific AI assistance duty role to those custom roles as needed, and then enable permission groups for those roles in Security Console.

## 💡 Tips and Considerations

• Use the Regenerate option to create a revised version of the draft change order. You can use it as many times as needed to guide the output towards your desired result. Note that regeneration creates a new version of the entire change order rather than updating specific sections.
• Provide sufficient details in the Initiate Change Order dialog box to generate more accurate and descriptive change orders.
• The system automatically generates the change order in your preferred language.

## 🔐 Access Requirements

To use this feature, you need the following duty role and privilege:

• Project Change Order Initiation Assistant (ORA_PRJ_PJE_CHANGE_ORDER_INITIATION_ASSISTANT_TEAM) duty role
• Manage Project Work Plan Data (PJT_MANAGE_WORK_PLAN_DATA) data privilege

This duty role and this privilege are included with the seeded Project Manager job role.

## 📚 Key Resources

• For more information about the original release of this capability, see the 24D What’s New topic, **Change Order Generation from Project Issue**.

---
*Oracle Cloud Readiness · 26C · ERP · Project Management*