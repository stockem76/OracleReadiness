[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Service Center](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/service-center.md)

# Operations Dashboard for Customer Service Managers

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/bsvc-26c/26C-b2b-service-wn-f46334.htm)

The Agentic Manager Operations Dashboard is an AI-powered workspace that helps Customer Service Managers monitor operations and act on the requests that need attention most. It brings together escalations, stalled service requests, and resolution performance into focused panels that surface critical signals, explain why they matter, and recommend next steps.

The Escalations experience identifies active escalated requests requiring manager attention, prioritizes them by urgency and business impact, and recommends actions such as reassignment or adding a qualified team member. Resource recommendations consider expertise, workload, similar issue history, customer context, and availability.

The Stalled Service Requests panel highlights requests that have started but are no longer progressing, ranks them by potential business impact, and recommends corrective action. The Resolution Performance panel tracks average resolution time and reopen rate to reveal throughput slowdowns, premature closures, or quality concerns.

Together, these capabilities help managers intervene earlier, maintain operational control, and improve service quality.

The Agentic Manager Operations Dashboard helps service organizations move from reactive monitoring to proactive operations management. It highlights escalations, stalled service requests, and resolution performance trends early, then provides AI-guided context and recommended actions so managers can prioritize effectively, intervene at the right time, and maintain consistent service quality.

• Helps managers identify high-risk escalations and stalled service requests before they impact customers.
• Improves prioritization by surfacing the work with the greatest urgency and business impact.
• Supports faster corrective action through AI-guided recommendations and resource suggestions.
• Improves workload distribution by helping managers assign work to qualified, available agents.
• Strengthens service quality by tracking resolution speed, reopen trends, and emerging performance issues.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• The Stalled Service Requests panel focuses on recently opened SRs, currently considering SRs opened in the past 30 days and in active execution states such as In Progress or Waiting.
• Stalled SRs are prioritized for impact, so the panel surfaces a focused set of high-priority items rather than every qualifying request.
• Escalation insights focus on active escalations that require manager attention; resolved requests or requests waiting on the customer are excluded.
• Resource recommendations depend on available signals such as workload, expertise, similar SR history, customer context, and availability.
• Resolution Performance reflects recent trends, using the latest 10-day window and comparing it with the preceding 10-day period to highlight changes in resolution time and reopen rates.

## 🔐 Access Requirements

To access the Agentic Manager Operations Dashboard, users must be assigned a custom role that includes the **Service Operations Workspace App User** duty role. After the role is assigned, users can launch and view the Service Operations Workspace dashboard panels.  After the access is granted, users may need to sign out and sign back in for the permission change to take effect.

More Information:

• Duty role: **Service Operations Workspace App User**
• Role code: 
  ORA_DR_SVC_AI_APP_SERVICE_OPERATIONS_WORKSPACE
• Privilege: 
  SVC_SERVICE_OPS_WKSP_APP_USER_PRIV
• Resource: 
  ORA_AIAPP_ORA_SERVICE_OPERATIONS_WORKSPACE

---
*Oracle Cloud Readiness · 26C · SERVICE · Service Center*