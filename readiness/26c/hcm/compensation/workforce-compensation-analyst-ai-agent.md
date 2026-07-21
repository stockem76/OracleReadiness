[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Compensation](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/compensation.md)

# Workforce Compensation Analyst AI Agent

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/comp-26c/26C-compensation-wn-f49766.htm)

Allow your worksheet managers to review plan information using the new Workforce Compensation Manager Analyst agent.  Managers can ask questions about:

• Status of reporting manager worksheets
• Overall budget info
• Manager due date info
• Manager overages

The agent operates in the context of the plan.  It doesn't provide info about individual employees, only individual managers status. It allows the manager to ask questions about the plan without navigating to one or more worksheet pages.

This agent is ideal for those managers that want to get plan info without multiple clicks.

Here are a few interactions with the AI agent:

Workforce Compensation Manager Analyst Agent Showing Budget Info

Agent Showing Budget Overage

Agent Showing Approval Status

Allows worksheet managers to ask questions with fewer clicks.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Compensation Management*

See the Global HR 25A release readiness topic:  AI Agent Task Type for Guided Journeys for info on how to configure your instance to use the new agent. The workflow agent name is Workforce Compensation Manager Analyst.

Once configured in Journeys:

1. Open the landing page for any plan
2. On the landing page, click the Profile icon in the top-right corner
3. Select Edit Page in Visual Builder Studio
4. Configure the Guided Journey in VB Studio
5. In Visual Builder Studio, enter the created Journey Code
6. Enter the created Journey.Task Code(s)
7. Click Publish

## 💡 Tips and Considerations

This agent will only provide info about summary or specific manager info.  In a future release you'll be able to ask about specific employee info.

---
*Oracle Cloud Readiness · 26C · HCM · Compensation*