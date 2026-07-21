[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Project Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/project-management.md)

# Project Change Summary Generation Assistant

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/ppm26c/26C-ppm-wn-f49454.htm)

Create a comprehensive summary of a project change order with a single click. The summary highlighting the impact of the change order on the project financials helps align stakeholders with project updates and eases approvals. The AI-generated summary can be easily edited and finalized, saving the project manager valuable time.

**Note:**Previously available in Prompt Lab, the 25B Project Change Order Summary Generation feature is now migrated to Fusion AI Studio.

The business benefits of this feature are as follows:

1. Streamlines stakeholder alignment, accelerates approvals, and supports informed decision-making with a comprehensive AI-generated change order summary.
2. Enables change order approvers and reviewers to quickly review summaries and take necessary actions directly from notifications while on the go, eliminating the need to navigate the application interface.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Project Execution Management*

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

To be able to access this feature, you need to do the following steps:

1. Enable the **Project Change Order Summary Generation** feature opt-in in the Project Execution Management offering in Setup and Maintenance**.**

  2. Enable the required permission groups in the Security Console for each role that you want to use with this feature.

**To enable permission groups:**

1. Navigate to **Navigator > Tools > Security Console** and click **Roles**.
2. Search for the job role you want to use with the AI-assisted feature and select **Edit Role**.
3. On the Basic Information page, click **Enable Permission Groups**, and confirm your choice.
4. Open the Role Hierarchy step. If needed, go to the Roles and Permission Groups tab and add the required feature-specific duty role and any required runtime duty role.
5. Click **Summary**, then click **Save and Close**.

If your organization uses custom roles, add the appropriate feature-specific AI assistance duty role to those custom roles as needed, and then enable permission groups for those roles in Security Console.

## 💡 Tips and Considerations

• Save the new change order before generating its summary.
• New and existing customers must opt in to use this AI-assisted feature. After opting in, enable the required permission groups.
• The system generates the change order summary in your preferred language if it’s supported under the Author/Summarize section here. For unsupported languages, the summary is provided in English.

## 🔐 Access Requirements

To use this feature, you need the following privilege and duty role:

• Manage Project Changes (PJE_MANAGE_PROJECT_CHANGE_PRIV)
• Project Change Summary Generation Assistant (ORA_PJE_PROJECT_CHANGE_SUMMARY_GENERATION_ASSISTANT_DUTY) This duty role is included in the seeded **Project Manager**and**Project Management Duty** role hierarchies.

## 📚 Key Resources

For more information about the original release of this capability, see the 25B What's New topic, Project Change Order Summary Generation

---
*Oracle Cloud Readiness · 26C · ERP · Project Management*