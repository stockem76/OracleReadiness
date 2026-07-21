[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Project Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/project-management.md)

# Program Performance Advisor

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/ppm26c/26C-ppm-wn-f49457.htm)

Drive program success with AI-enabled program analysis and actionable plans. Oracle AI helps uncover program-specific trends and generates actionable recommendations, empowering data-driven decision-making and optimizing program execution.

In seconds, AI analyzes key performance metrics to provide a concise overview of the program’s current state and identifies up to 5 critical projects that require immediate attention; a task that would typically take hours to complete manually. As the Program Manager receives tailored recommendations for each identified project, they can take swift and decisive action to quickly transform these insights into actionable plans with pre-filled descriptions and action items.

**NOTE:**Previously available in Prompt Lab, the 25A Project Program Analysis and Action Plan Generation feature is now migrated to Fusion AI Agent Studio.

Business benefits include:

• **Data-Driven Decision Making:** Make informed choices based on accurate and timely insights.
• **Improved Program Performance:** Identify and address potential issues before they escalate.
• **Enhanced Efficiency:** Automate routine tasks and focus on strategic initiatives.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Project Financial Management*

To be able to access this feature, you need to do the followings steps.

  1. Enable the FSM opt-in **Project Program Analysis and Action Plan Generation.**

  2. Enable the required permission groups in the Security Console for each role that you want to use with this feature.

**Steps to Enable Permission Groups:**

1. Navigate to Navigator > Tools > Security Console and click **Roles**.
2. Search for the job role that you want to use for the generative AI feature and select **Edit Role**.
3. On the role Basic Information page, click **Enable Permission Groups**, and confirm your choice.
4. Open the **Role Hierarchy** step. If needed, go to the Roles and Permission Groups tab and add the required feature specific duty role and any required runtime duty role.
5. Click Summary, and then click Save and Close.

If your organization uses custom roles, add the appropriate feature-specific AI assistance duty role to those custom roles as needed, and then enable permission groups for those roles in the Security Console.

## 💡 Tips and Considerations

• Both new and existing customers must opt-in to use this Oracle AI-powered feature. Once opted-in, you can immediately access program insights.

• For even more accurate and impactful insights, ensure your project and program data is as comprehensive as possible. Include detailed budgets, forecasts, action plans, and clear project/program names and descriptions while creating your project/programs.

## 🔐 Access Requirements

To use this feature you need the following role and privilege:

• Program Performance Advisor (ORA_PJS_PROGRAM_PERFORMANCE_ADVISOR_DUTY) duty role.
• Manage Project Program (PJS_MANAGE_PROJECT_PROGRAM) privilege.

These duty roles and privileges are included with the seeded Program Manager job role.

## 📚 Key Resources

• For more information about the original release of this capability, see the 25A What’s New topic, **Project Program Analysis and Action Plan Generation**.

---
*Oracle Cloud Readiness · 26C · ERP · Project Management*