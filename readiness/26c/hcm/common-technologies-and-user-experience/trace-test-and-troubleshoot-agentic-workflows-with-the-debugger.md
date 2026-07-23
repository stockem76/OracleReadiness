[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Common Technologies and User Experience](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/common-technologies-and-user-experience.md)

# Trace, Test, and Troubleshoot Agentic Workflows with the Debugger

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/common/26c/common26c/26C-common-wn-f50065.htm)

Debugger is a powerful tool in AI Agent Studio that helps you trace, test, and troubleshoot agentic flows in real time. It provides deep visibility into node execution, context, inputs, outputs, and LLM reasoning, making it easier to understand how a flow behaves during runtime. You can use Debugger to do these tasks:

• Run an agentic flow using a realistic user prompt or a saved run profile.
• Visually trace the execution path taken for your question or message.
• Confirm which nodes completed successfully.
• Inspect each node’s inputs, outputs, variables, and context.
• Set a break point to pause execution at a node and continue one step at a time.
• Override node configurations and test your changes live in the debugger.
• Rerun the workflow from a specific node after changing or inspecting data.
• Pin or override a node’s output to test downstream behavior without rerunning upstream dependencies.
• Manage your test cases using run profiles.

Debugger helps you validate agent behavior before publishing. It shows how a request flows through the agent, what inputs are passed to each node, what outputs are returned, and how the final response is generated. This reduces trial and error and makes defects easier to isolate. The Debugger tool supports the following tasks:

• Shorten build cycles: Agent creators can rerun from a specific node instead of replaying the entire agentic flow.
• Improve quality before release: Teams can catch incorrect routing, malformed payloads, poor tool responses, and weak summaries during design time.
• Increase agent reliability: Saved run profiles make common scenarios repeatable.
• Lower operational risk: Step-through debugging and output inspection make it easier to understand why an agent made a particular decision.
• Accelerate root-cause analysis: When an answer is incorrect, teams can trace the issue back to the node where it originated.

## ⚙️ Steps to Enable and Configure

You must have access to use AI Agent Studio.

## 🔐 Access Requirements

Access Requirements for AI Agent Studio

---
*Oracle Cloud Readiness · 26C · HCM · Common Technologies and User Experience*