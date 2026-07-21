[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Service Center](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/service-center.md)

# Service Request Resolution Workflow Advisor Enhancements

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/bsvc-26c/26C-b2b-service-wn-f47298.htm)

The Service Request Resolution Workflow Advisor is enhanced with **Human-in-the-Loop (HIL)**, **follow-up handling**, and**rejection handling** within the resolution workflow. These capabilities allow organizations to control when a Service Request is resolved autonomously, when it is routed for human review, and how follow-up or rejected interactions are handled without breaking the workflow.

With HIL, the workflow can route selected resolutions for CSR review through an Action Plan rather than sending a response directly to the customer. With follow-up handling, customers or CSRs can continue the interaction with additional details or clarifications while preserving context. With rejection handling, the workflow can refine the resolution when an outcome is not accepted, using bounded retries to avoid repeated execution and infinite loops.

These enhancements are particularly valuable during early stages of AI adoption, in sensitive or high-impact scenarios, and in environments where additional oversight is required for less mature processes or products.

**What is introduced**

Human-in-the-Loop (HIL)

• HIL flag (default: false) is set via Automation Rules and passed with the Service Request to the resolution workflow
• HIL = false: Resolution is generated and sent directly to the customer; the Service Request is marked resolved
• HIL = true: Resolution is routed as an Action Plan to CSR for review before customer communication

Follow-up Handling

• Customer interactions such as questions or additional details are routed back into the same workflow
• CSR can refine, adjust, or validate responses before final resolution
• The workflow maintains the same interaction context across follow-ups

Rejection Handling

• Detects when a resolution is not accepted and avoids blind re-execution
• Applies bounded retries (default: up to 3 attempts) to prevent infinite loops

**Business Value**:

• **Controlled automation**: apply HIL for governance in sensitive or high-impact scenarios
• **Higher resolution accuracy**: iterative follow-ups and rejection handling refine outcomes
• **Eliminates rework loops**: avoids repeated, ineffective executions with bounded retries
• **Better customer experience**: supports natural interactions (questions, clarifications) within the same flow
• **Operational efficiency**: keeps review and retries within a single workflow

## ⚙️ Steps to Enable and Configure

Pre-Requisite: Upgrade to 26C

Create Automation Rules Action -> set HIL parameter to true -> create Automation Rule with conditions and add the created action -> deploy -> test with SR

  Note: For a template-based AI Agent, the AI Agent must also be configured and published before use.

**Step 0 (Optional): Configure the AI Agent Team in Agent Studio**

Follow this step only if you want to use a custom agent built from templates

• Template name: Service Request Resolution Workflow Advisor
• Navigate to: Tools > Agent Studio
• If you use a template-based custom agent, clone both Service Request Resolution Assistant and Service Request Resolution Workflow Advisor templates, make the required changes, and then publish the agents
• Adjust the agent team Name and Team Code to match your custom configuration
• Use the same naming and code values consistently across Agent Studio and Automation Rules

**Step 1: Set Channel Id in the AI Agent workflow**

This step ensures responses are routed through the correct communication channel (for example, Email)

• Identify the channelId for ORA_SVC_EMAIL in the target environment using crmRestApi/resources/11.13.18.05/channels
• Search for the channel name ORA_SVC_EMAIL and note the corresponding channelId value; this value can differ by environment
• Go to the Agent Studio, open the Service Request Resolution Workflow Advisor agent, and under Send Agent Response Node, replace the fetch message BO with Inbound SR Messages
• Update the response payload so it includes the correct channelId value for the selected channel
• Use the channelId in the payload to ensure the response is routed through the correct communication channel
• If needed, validate the channel mapping before deploying to production

**Sample:**

`let messageContentVar = $context.$nodes.REQUEST_INFO_EVAL.$output.Summary;
let partyViaEndPointVar = $context.$nodes.GET_SR_DATA.$output.PrimaryContactEmailAddress;
let partyIdVar = $context.$nodes.GET_SR_DATA.$output.PrimaryContactPartyId;
let title = $context.$nodes.GET_SR_DATA.$output.Title;
let srNumber = $context.$triggers.REST.$input.objectNumber;`

`const payload = {
  MessageTypeCd: "ORA_SVC_RESPONSE",
  ChannelTypeCd: "ORA_SVC_EMAIL",
  StatusCd: "ORA_SVC_COMMITTED",
  SourceCd: "ORA_SVC_REDWOOD_AGENT_UI",
  Subject: srNumber + " - " + title + " (AI Agent Generated)",
  MessageContent: messageContentVar
};`

`if (partyViaEndPointVar) {
  payload.channelCommunication = [
    {
      ChannelId: "<channelId>",
      PartyViaEndPoint: partyViaEndPointVar,
      RoutingCd: "ORA_SVC_TO",
      PartyId: partyIdVar
    }
  ];
}`

`return payload;`

**Note:**The above is only a sample and should not be used directly without proper testing.

**Step 2: Create Action**

This step configures how the Service Request triggers the Resolution Workflow

• Go to: Service > Service Centre administration > Productivity > Add/Manage Automation Rules Action Types and Actions
• Use this area to define the automation rule action that triggers the Resolution Workflow

Minimum required to get started: Agent team Name, Action URL, API User, parameters (objectNumber, objectType, HIL)

• Configure the action with the fields: 
  • **Action Type Object Name**: Service request
• **Application**: Oracle Fusion Applications
• **Authentication Context:** Oracle AI Agent Studio
• **Family**: CX
• **Product**: Service
• **Agent team Name**: <Agent Team Name> (*use****Service Request Workflow Advisor RA****for runnable agent or the corresponding name from Agent Studio)*
• ActionType: Rest
• Operation: Create
• Action URL: api/fusion-ai/orchestrator/agent/v2/<Team_Code>/invokeAsync (*use **SERVICE_REQUEST_WORKFLOW_ADVISOR_RA** for runnable agent or the corresponding Team Code from Agent Studio*)
• Description: provide any description to help understand the configuration later
• API User Type Code: Integration User
• API User: provide the username that will be used for authentication with AI Agent Studio
• Configure parameters supported by the Resolution Workflow: 
  • HIL — true or false (default: false)
• objectNumber — unique identifier, for example {{$SrNumber}}
• objectType — for example ServiceRequest
• Optional: persona, objectContext, conversationContext, skipValidation, skipClassification, isVectorSearchEnabled, publishResolution

**Asynchronous Mode / Polling**

Required for asynchronous execution and response polling from the AI Agent (Some details will be auto-populated)

• Set to Async with Polling
• Maximum Polling Count: 3
• Success key: status
• Success value: COMPLETE
• Polling URL: api/fusion-ai/orchestrator/agent/v2/<Team_Code> (*use **SERVICE_REQUEST_WORKFLOW_ADVISOR_RA** for runnable agent or the corresponding Team Code from Agent Studio*)
• Request Id key: jobId

**Step 3: Create Automation Rule**

• Navigate to: Productivity > Create and Manage Automation Rules
• Create a rule with: 
  • Conditions: when to trigger
• Action: select the action from Step 2

Example

• Condition: 
  • SR Severity = High
• Channel = Email
• Action parameter: 
  • HIL = true
• Result: SR is routed to CSR for review before resolution

**Follow-ups from UI**

  Configuration is required only for customization

• For customization: 
  • Use skipValidation = true, skipClassification = true, HIL = true
• conversationContext should match the original AI workflow request message ID
• For OOB scenarios, this is handled automatically

## 💡 Tips and Considerations

• Use HIL selectively for high-risk or low-confidence scenarios
• Gradually expand autonomous resolution as confidence improves
• Configure and validate the workflow in a sandbox environment and promote to production after validation

## 🔐 Access Requirements

• Roles and permissions required to access **Service** **Automation Rules (Formerly Service Workflow)**
• Roles and permissions required to access **AI Agent Studio**

---
*Oracle Cloud Readiness · 26C · SERVICE · Service Center*