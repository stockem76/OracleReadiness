[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Project Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/project-management.md)

# Project Proposal Generation Assistant

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/ppm26c/26C-ppm-wn-f49461.htm)

Create a comprehensive project proposal that covers project objectives, scope, timeline, budget estimates, and staffing plans, using Oracle AI during project planning. Project managers can easily edit and finalize the proposal, saving time and improving efficiency. For example, when starting projects from advanced sales opportunities, use the project proposal to clearly communicate the project's goals, scope, and expected outcomes to stakeholders, securing the required funding and resources.

Project managers can efficiently create detailed project proposals from the **Project Management work area** through the action panel under **Manage Project Proposals**, reducing manual effort and improving accuracy.

As part of the proposal generation, quickly review the project details and make necessary adjustments before generating a complete proposal with a **single click.**

**Note:**Previously available in Prompt Lab, the 25B Project Proposal Generation feature is now migrated to Fusion AI Studio.

The business benefits of this feature are as follows:

• Significantly reduces proposal creation time, minimizes manual errors, and improves efficiency.
• Enables project managers to quickly refine automatically generated project proposals to align with specific client requirements.
• Allows project stakeholders to make informed decisions faster, helping secure the necessary funding and resources without delays.
• Enables organizations to respond rapidly to advanced sales opportunities, increasing their chances of winning projects by presenting well-defined plans to clients.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Project Financial Management*

Use the Opt-In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

To access this feature, complete the following steps:

• Enable the Project Proposal Generation feature opt-in in the Project Financial Management offering in Setup and Maintenance.
• Enable the required permission groups in Security Console for each role that will use this feature.

**Steps to Enable Permission Groups:**

1. Navigate to Navigator > Tools > Security Console and click **Roles**.
2. Search for the job role that you want to use for the AI-assisted feature and select **Edit Role**.
3. On the role Basic Information page, click **Enable Permission Groups**, and confirm your choice.
4. Open the **Role Hierarchy** step. If needed, go to the Roles and Permission Groups tab and add the required feature-specific duty role and any required runtime duty role.
5. Click **Summary**, and then click **Save and Close**.

If your organization uses custom roles, add the appropriate feature-specific AI assistance duty role to those custom roles as needed, and then enable permission groups for those roles in the Security Console.

## 💡 Tips and Considerations

• To use this generative AI-powered feature, both new and existing customers need to opt in. Once opted in, you can immediately start generating project proposals.
• The system automatically generates the project proposal in your preferred language if it's one of the languages mentioned under the Author/Summarize section here. For other languages, the summary is provided in English.
• For accurate and impactful project proposals, ensure the project includes a high-level plan, budget, and clear description.

## 🔐 Access Requirements

To use this feature, you need the following functional, data, and duty privileges:

• Manage Project Proposal (PJF_MANAGE_PROJECT_PROPOSAL_PRIV)
• Manage Project Proposal Data (PJF_MANAGE_PROJECT_PROPOSAL_DATA)
• Project Proposal Generation Assistant (ORA_PJF_PROJECT_PROPOSAL_GENERATION_ASSISTANT_DUTY)

If you use custom roles instead of the predefined job role above, you must assign the Manage Project Proposal privilege to your custom roles to use this feature.

## 📚 Key Resources

For more information about the original release of this capability, see the 25B What's New topic, Project Proposal Generation

---
*Oracle Cloud Readiness · 26C · ERP · Project Management*