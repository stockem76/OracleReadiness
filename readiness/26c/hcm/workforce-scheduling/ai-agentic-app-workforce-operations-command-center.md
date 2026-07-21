[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Workforce Scheduling](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/workforce-scheduling.md)

# AI Agentic App: Workforce Operations Command Center

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/wosc-26c/26C-workforce-scheduling-wn-f49778.htm)

Use Workforce Operations Command Center, an AI-powered agentic app, to quickly review and act on urgent workforce issues across scheduling, absences, and time cards. It’s a system of outcomes where an orchestrator coordinates specialist workforce agents to continuously reason over real-time operational conditions, share context across schedules, absences, and time, and advance work forward with recommended actions that keep coverage intact and get timecards ready for payroll processing.

The key capabilities include:

• Summary: AI-generated summary on operational status across scheduling, absences and time.
• Top Priorities: A focused list of priority items that affect coverage, compliance, or payroll readiness. It includes absences that overlap with shifts, pending shift requests for today and tomorrow, and prior-period timecard issues. Items are ordered by severity and by domain so you know what to handle first.
• Priority Actions: Review and act on recommended actions, including approving shift drop requests and absences, reassigning the resulting open shifts, and approving shift requests from worker—all for the same day.
• Absence Overview: Review upcoming absence requests that are pending approval with clear indicators for shift conflicts and potential overlaps. Approve absences in bulk where there are no conflicts or review items individually with full context.
• Schedule Overview: Track current and near-future schedule periods for open shifts, violations, and publication status. Publish overdue schedules in a single action and use severity indicators to focus attention.
• Time Overview: Monitor timecard readiness for payroll with a visual breakdown of statuses, including missing and errored timecards. Submit timecards in bulk or approve submitted timecards; review a detailed exceptions panel.
• Workforce Trends: Compare fill rates across the last and current schedule periods by department to spot coverage gaps and improvements.
• Communications: Generate targeted outreach to employees and payroll managers or administrators. Managers can request corrections for incomplete or error timecards, prompt employees to create missing timecards, or notify payroll managers about timecards that are pending transfer. Recipient lists and draft content are pre-populated.
• Workforce Summary communication can also generate a downloadable presentation with top priorities and recommended actions.
• Ask Oracle: Ask natural-language questions about schedules, absences, and time.

No additional functional setup is described for the app itself. Grant access to the appropriate users and confirm that their existing data roles, security profiles, and domain privileges support the workers, departments, and actions they need.

Accelerate decision-making with a single view of urgent workforce signals and one-click guided actions, while reducing coverage risk and payroll delays through proactive alerts, bulk actions, and targeted communication.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• Top priorities focus on urgent items that need immediate action, while the overview sections provide broader operational context.
• Available actions depend on the schedule, absence, time card and approval privileges granted to the user.
• After submitting or approving time cards through an ESS job, the time overview chart might not update immediately.

## 🔐 Access Requirements

The Workforce Operations Command Center can be accessed through My Client Groups > Workforce Scheduling > Workforce Operations Command Center. Access is secured by the corresponding function privilege, which allows users to open and use the Workforce Operations Command Center.

Privilege | Code | Description
Access Workforce Operations Command Center | HWM_ACCESS_WORKFORCE_OPERATIONS_COMMAND_CENTER | Allows users to access the workforce operations command center.

To generate the Workforce Summary document, you also need to include the **Read DocumentGenConversion REST Resource** permission group.

The Workforce Operations Command Center is designed for workforce managers. Access to information and available actions is determined by the user’s assigned roles, data roles, and security profiles. 

  A typical configuration may include:

• Line Manager role with a data role aligned to the manager hierarchy
• Time and Labor Manager role with an appropriate data role
• Workforce Schedule Manager role with defined areas of responsibility
• Employee role with a Transaction Security Profile–based security profile

Users can only view workers and departments within their security scope. Available actions—such as approving absences, publishing schedules, and submitting or approving timecards—depend on the privileges granted through these roles.

---
*Oracle Cloud Readiness · 26C · HCM · Workforce Scheduling*