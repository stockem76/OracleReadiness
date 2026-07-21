[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Service Center](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/service-center.md)

# View and Customize Seeded Policy Models in AI Agent Studio

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/bsvc-26c/26C-b2b-service-wn-f50291.htm)

You can now create policy models in AI Agent Studio to enable reliable, repeatable, and deterministic policy-based decision-making at runtime. Policy models transform business policies into executable logic that agents can use to consistently evaluate rules, calculations, and decisions in agentic workflows. To help you get started, AI Agent Studio includes seven seeded policy models that can be viewed, explored, and customized for service-related scenarios. These examples show service administrators, implementers, and subject matter experts how policy inputs, outputs, rules, specifications, and test cases work together to support consistent policy-based decisions. You can use the seeded models as starting points for understanding and tailoring policy logic for workflows such as payment arrangements, returns routing, warranty coverage, eligibility assessments, and fee or benefit calculations.

The seeded policy models available in 26C are:

• **Payment Plan Payments**: Calculates payment dates and installment amounts for customers who are behind on utility bills.
• **Education Prior Learning Credits**: Determines whether completed studies can be recognized as prior learning or qualify for tuition credit or reimbursement.
• **Telecommunications OEM Return Dispositions**: Evaluates complex device return requests and determines approval, routing, priority, and disposition details.
• **Hotel Stay Franchise Fees**: Calculates stay-based franchise fees using stay, membership, and discount details.
• **Telecommunications Shared Pole Fees**: Calculates rental fees for telecommunications providers using shared infrastructure, such as poles or towers.
• **Manufacturing Solar Warranty Eligibilit**y: Determines the extent to which a repair is covered under warranty.
• **International Prescribed Benefit Pension Payments**: Calculates prescribed benefit pension payment amounts for eligible retirees.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

To view and customize seeded policy models: 

  1.    In the new AI Agent Studio user interface, select **Policy**in the left navigation menu.

  2.    In the main pane, select the **Policy**tab.

  3.    Open a published seeded policy model to view it. Seeded policy models have a **Seeded**badge next to the name and a **Published**status. Published seeded policy models are read-only baseline examples and can’t be edited or deleted directly.

  4.    Select **Customize** to create a copy of the policy model for editing while preserving the original seeded model. After you publish your customized version, you can add it to a workflow as a policy node. The published version remains the version used by the workflow until a newer version is published. This allows policy customization without requiring the workflow itself to be edited again.

**Disclaimer**: These seeded policy models are for demonstration and exploration purposes only. While the policies are based on real-world scenarios, Oracle makes no representations or warranties regarding their accuracy, completeness, suitability, or compliance. Do not use them as is in production. Independently validate and tailor the examples for your environment.

## 🔐 Access Requirements

Roles and permissions required to access AI Agent Studio

## 📚 Key Resources

• Create Policy Models in AI Agent Studio Interface
• 26C Seeded Policy Model files - This ZIP contains the policy documents and test documents that were uploaded to create the seeded policy models in AI Agent Studio

---
*Oracle Cloud Readiness · 26C · SERVICE · Service Center*