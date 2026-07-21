[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Work Life](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/work-life.md)

# Redwood Experience for Corporate Citizenship

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/woli-26c/26C-worklife-wn-f49929.htm)

The Redwood experience for Corporate Citizenship concentrates on the Volunteering flows that matter most during rollout. The employee experience uses guided steps and action-focused pages so users can sign up, find relevant opportunities, and stay engaged after they join or create a project. The administrator experience centralizes approvals, communications, and feature configuration in the Corporate Citizenship Administration workspace.

• Employees can use preferences such as causes, location, and interest in leading projects to influence recommendations.
• Project creation captures organization details, scheduling, location, featured image, benefits, and supporting attachments in a structured sequence.
• Administrators can manage approvals, campaigns, newsletters, project feedback, surveys, settings, and data connectors from the same volunteering administration footprint.

Corporate Citizenship now supports a Redwood-style experience for volunteering tasks that employees and administrators perform throughout the program lifecycle. Here's how employees can navigate to Corporate Citizenship from the UI: **Me > Corporate Citizenship > Volunteering**.Using this feature they can register for volunteering, discover and join projects, create projects, manage their own project activity, maintain preferences and teams, and review rewards when that integration is enabled.

Administrators navigate to Corporate Citizenship by using this navigation: **My Client Groups > Corporate Citizenship Administration > Volunteering**. They can use this feature to review projects and organizations, create campaigns and newsletters, manage settings and surveys, moderate completion photos, and maintain the integrations that support the volunteering program.

This table shows how Corporate Citizenship works for employees and administrators:

Employee Self-Service | Administrator Workspace
Complete first-time registration before volunteering or creating projects. | Review and approve projects, organizations, and completion photos.
Search recommended and available projects by cause, location, date, and participation type. | Create and update campaigns, newsletters, surveys, and volunteering settings.
Create volunteering projects with a guided six-step flow. | Maintain EIN validation, causes, user agreement content, rewards integration, and data connectors.
Track projects, campaigns, teams, preferences, social connectors, and rewards when configured. | Validate end-to-end access for employees and project leads before rollout.

**Employee Experience Highlights**

• **Access Corporate Citizenship and complete registration:** From the Me landing page, employees open Corporate Citizenship and select Volunteering. First-time users complete an initial registration flow before they volunteer for a project or submit a new project. Registration covers profile details, participation settings, and the agreements that administrators configure for the volunteering program.
• **Discover, join, and track volunteering projects:** The Find Projects page displays recommended and available projects. Employees can search and filter by cause, location, date range, and participation type, review project details, and volunteer directly from the project they select. My Projects provides visibility for enrolled, invited, completed, and in-review work so users can keep track of current status and available actions.
• **Create new volunteering projects:** Employees can create a volunteering project through a guided six-step flow that covers organization details, project details, address, featured image, volunteer benefits, and attachments before submission. Project owners can also revisit project rows in My Projects to manage actions such as edit, copy, team management, and project follow-up where those actions are available for their role.
• **Stay engaged through teams, preferences, and rewards:** The Redwood experience also supports ongoing engagement activities. Employees can maintain profile preferences, join or create volunteering teams, connect supported social channels when their organization enables those integrations, and review rewards activity and catalog items when CrowdTwist rewards are configured.

**Administrator Experience Highlights**

• **Open the volunteering administration workspace:** Administrators open Corporate Citizenship Administration from My Client Groups and then select Volunteering. That landing page becomes the centralized administration workspace for projects, organizations, campaigns, newsletters, surveys, settings, and connector management.
• **Review projects, organizations, and photos:** The Projects page lets administrators review submitted records, apply filters such as project state, cause, location, and photo approval status, and then approve, return, reject, or inactivate projects as appropriate. The Organizations page supports review and approval of submitted organization records, including EIN validation considerations for US-based organizations. Administrators also moderate completion photos before those images appear to end users.
• **Manage campaigns, feedback, and communications:** Campaigns group related volunteering projects under a common initiative. Administrators can review existing campaigns, create new campaigns, add eligible projects, and monitor campaign status. The same workspace also supports project feedback review and newsletter creation so administrators can manage communications for volunteers and project leads.
• **Maintain settings, surveys, and integrations:** Settings control the user agreement, photo approval behavior, causes, EIN validation schedule, and rewards integration that shape the employee experience. Administrators can also maintain the survey configuration used in volunteering processes and review data connectors for channels such as Facebook, LinkedIn, X, Slack, and other enabled integrations.

Enhances user experience and visual consistency, helping users interact with the dashboard more efficiently and confidently.

## ⚙️ Steps to Enable and Configure

• Provision employee and administrator access to Corporate Citizenship. Use predefined roles where possible, and for custom roles map the privileges required for Volunteering and Volunteering Administration flows.
• Confirm the navigation entry points are available to each audience. Employees should see Corporate Citizenship from Me, and administrators should see Corporate Citizenship Administration from My Client Groups.
• Review volunteering settings before rollout. Configure user agreement content, photo approval behavior, causes, EIN validation, and rewards integration according to your program design.
• Validate employee readiness by completing first-time registration, browsing projects, creating a project, reviewing My Projects, updating profile preferences, and checking team and rewards visibility where relevant.
• Validate administrator readiness by reviewing project approvals, organization review, campaign creation, newsletter setup and preview, survey maintenance, and connector visibility in the administration workspace.
• Run end-to-end access testing with at least one employee and one administrator so permission issues are discovered before broader adoption.

## 💡 Tips and Considerations

• Employees need to finish first-time registration before they can volunteer for a project or create one.
• Recommended projects depend on the preferences employees set, including causes and location.
• The Campaigns page focuses on ongoing campaigns; future or completed campaigns may be presented differently from the active landing view.
• Completion photos require administrator approval before they appear in the experience.
• Reward pages are visible only when CrowdTwist integration is configured and enabled.
• Social media connectors and other external channels appear only when your organization configures them.
• After administrators finish newsletter setup, run the Generate Notifications ESS process so eligible bell and email notifications are issued.
• Include access validation in deployment readiness checks because employees can't assign roles to themselves.

## 🔐 Access Requirements

Access to Corporate Citizenship Volunteering is controlled through role assignment. After the upgrade, assign the required employee duty role and administrator job role. If you use custom job roles, perform Enable Permission Groups so the role is SaaS-enabled before you validate user access.

Audience or Setup Area | Corporate Citizenship Requirement
Employees | After the upgrade, assign the duty role ORA_DR_GTG_CORPORATE_SOCIAL_RESPONSIBILITY_EMPLOYEE_DUTY so employees can access the volunteering pages.
Administrators | Assign the role ORA_HHR_CORPORATE_SOCIAL_RESPONSIBILITY_MANAGER_JOB so administrators can access Corporate Citizenship Administration and the volunteering work area.
Custom job roles | Perform Enable Permission Groups so the custom job role is SaaS-enabled before you validate access.
Readiness validation | Include employee and administrator role checks in deployment readiness because users can't grant roles to themselves.

---
*Oracle Cloud Readiness · 26C · HCM · Work Life*