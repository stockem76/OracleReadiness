[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Service Center](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/service-center.md)

# CX Service Global Functions Now Powered by Runnable AI Agents

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/bsvc-26c/26C-b2b-service-wn-f46435.htm)

This feature aligns key CX Service Global Functions with the runnable AI Agent architecture in AI Agent Studio.

The following Global Functions are updated to use runnable AI Agents instead of the previous REST-based implementation:

• SR Overview
• SR Problem Description
• SR Solution

These functions now leverage the **ORA_SERVICE_REQUEST_SUMMARIZATION_ASSISTANT_RA** agent with different prompt configurations:

• SR Overview - SR_Summarization
• SR Problem Description - SR_Problem_Summarization
• SR Solution - SR_Solution_Summarization

This standardizes how AI capabilities are executed across CX Service by using a unified, agent-based framework.

• Ensures architectural consistency across AI-powered features
• Simplifies extensibility to modify the seeded prompts of these agents within AI Agent Studio
• Enhances observability and control of AI executions

## ⚙️ Steps to Enable and Configure

Leverage the Visual Builder Studio to expose your applications. To learn more about extending your application using Visual Builder, visit Oracle Help Center > *your apps service area of interest* > Books > Configuration and Extension.

1. Navigate to **Oracle Visual Builder Studio** for CX Service.
2. Create or edit an existing Action Chain. 
  • Identify existing Global Functions (AI Assist, SR Overview, SR Problem Description, SR Solution).
3. If needed you configure the AI Agent (AI Agent Studio): 
  • Select **ORA_SERVICE_REQUEST_SUMMARIZATION_ASSISTANT_RA**
• Set the appropriate promptCode: 
    • SR_Summarization for SR Overview
• SR_Problem_Summarization for Problem Description
• SR_Solution_Summarization for Solution
4. Validate the configuration in a test environment by triggering each Global Function.
5. Deploy changes to production after successful validation.

## 💡 Tips and Considerations

n/a

## 🔐 Access Requirements

• Oracle Visual Builder Studio for Application Extension

## 📚 Key Resources

n/a

---
*Oracle Cloud Readiness · 26C · SERVICE · Service Center*