[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Common Technologies and User Experience](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/common-technologies-and-user-experience.md)

# Long-Term Memory Support for Agents

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/common/26c/common26c/26C-common-wn-f50078.htm)

Agents now support long-term memory, enabling them to retain useful context from previous user interactions and deliver more personalized and relevant experiences. Long-term memory consists of two components: episodic memory and user preferences.

Episodic memory captures summaries of past interactions, tasks, cases, and activities performed through agent conversations. These summaries, known as memory notes, are automatically generated through a memory curation process that runs at regular intervals throughout the day. Memory notes are maintained per user and per agent and can include relevant account and interaction context. When a user engages with an agent, the system automatically performs a semantic search across stored memory notes to identify relevant historical context. The retrieved memory notes are added to the current conversation context, enabling the agent to generate responses and perform tasks with greater continuity and contextual awareness.

User preferences store information about how a user prefers agents to respond, such as preferred formats, tone, communication style, or level of detail. Unlike episodic memory, user preferences are shared across agents, allowing users to receive a more consistent experience regardless of which agent they interact with.

This feature enables organizations to deliver more personalized and context-aware agent experiences by leveraging knowledge gained from previous user interactions. Episodic memory improves task efficiency by helping agents maintain continuity across conversations, reducing the need for users to repeatedly provide the same information. User preferences allow agents to consistently align responses with individual user expectations, enhancing user satisfaction and engagement. These capabilities improve productivity, accelerate task completion, and create more relevant and effective interactions across agent-driven experiences.

## ⚙️ Steps to Enable and Configure

You must have access to use AI Agent Studio.

## 🔐 Access Requirements

Access Requirements for AI Agent Studio

---
*Oracle Cloud Readiness · 26C · HCM · Common Technologies and User Experience*