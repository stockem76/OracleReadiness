[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Service Center](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/service-center.md)

# Multi-task more naturally across SRs and interactions while conversing with AI agents

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/bsvc-26c/26C-b2b-service-wn-f46436.htm)

This enhancement enables service representatives to interact with the **AI Agent chat in a persistent, non-modal panel** embedded directly within the Service Console. Instead of opening in an overlay drawer. The AI conversation panel is now displayed inline within each tab, allowing agents to continue their work without interruption.

Also, you can now use **Inline mode** when configuring the **CX Service: AI Agent – Launch Agent Team UI** action chain in Oracle Visual Builder Studio.

The experience is designed for multitasking across multiple Service Center workspace tabs:

• The AI chat is **embedded within each tab**, providing a contextual experience
• **Chat context is preserved per tab and per customer interaction**, ensuring continuity
• Service reps can **switch between tabs without losing conversation history**, improving efficiency and reducing repeated inputs

This results in a more seamless, focused, and productive interaction model when interacting conversationally with AI Agents.

**Example Use Cases**

• A service rep works on multiple Service Requests in different tabs and interacts with the AI Agent in each tab without losing conversation context
• An service rep pauses a conversation with the AI Agent on one customer record, switches to another tab, and later resumes the same conversation seamlessly
• Organizations enable AI assistance directly within the Service Console to support real-time decision-making without disrupting workflows
• Service reps use the inline AI conversation panel alongside ongoing tasks (for example, reviewing SR details or updating fields) without navigating away from the current page
• Developers configure AI Agent launch behavior to provide a consistent, embedded experience across all Service Center interactions

• Improves user productivity by removing context switching friction
• Reduces repetitive inputs by preserving AI conversation history
• Enables faster issue resolution with continuous AI assistance
• Supports true multitasking across multiple customer interactions

## ⚙️ Steps to Enable and Configure

### **Steps to Enable / Use**

1. The **AI Inline Chat Panel** is enabled by default—no setup is required
2. In any **Service Center** page, locate the **Oracle AI Assistant icon** in the action bar
3. Click the **AI Assistant icon** to launch the panel
4. The **AI Inline Chat Panel** opens on the left side of the screen
5. Start interacting with the AI Agent directly within the panel

**Extensibility Option:**

1. Open **Oracle Visual Builder Studio**
2. Navigate to your **Service Center extension project**
3. Locate or create an **Action Chain**
4. Add the action: **CX Service: AI Agent – Launch Agent Team UI**
5. In the action properties, select **Inline mode** as the display option
6. Save and publish your changes
7. Run the application and trigger the action:
• The AI Agent will open **inline within the current page** instead of a separate view

## 💡 Tips and Considerations

n/a

## 🔐 Access Requirements

• Oracle Visual Builder Studio for Application Extension

## 📚 Key Resources

n/a

---
*Oracle Cloud Readiness · 26C · SERVICE · Service Center*