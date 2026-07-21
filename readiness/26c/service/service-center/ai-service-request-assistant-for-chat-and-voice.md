[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Service Center](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/service-center.md)

# AI Service Request Assistant for Chat and Voice

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/bsvc-26c/26C-b2b-service-wn-f43927.htm)

This feature enables a customer service representative to rapidly create a Service Request (SR) either at the end of a chat/phone call (based on the recommendation) or during an active interaction (using a smart action). As part of the Create SR action, when there is sufficient contextual information available in the interaction metadata and conversation transcript, the AI agent automatically generates and populates fields on the newly created SR.

Automatic populate of SR fields using the AI Assistant eliminates the need for agents to manually transcribe interaction details into service requests, helping to shorten wrap up time and capture more complete, consistent SR data..

## ⚙️ Steps to Enable and Configure

In order to allow access to the Create SR AI Agent API, the ORA_DR_SVC_GEN_AI_USER_DUTY duty role needs to be assigned to the job role used by your Customer Service Representative (CSR).  This duty role is already assigned to most of the pre-seeded Service job roles.

Note: By default the "ORA_SERVICE_REQUEST_CREATION_ASSISTANT_WF_RA"  agent team is used to generate SR details.

## 💡 Tips and Considerations

An AI loading animation is shown while the information is being pre-populated, and the animation becomes static once the data is populated.

---
*Oracle Cloud Readiness · 26C · SERVICE · Service Center*