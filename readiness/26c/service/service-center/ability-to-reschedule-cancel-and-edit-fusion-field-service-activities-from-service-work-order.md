[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Service Center](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/service-center.md)

# Ability to Reschedule, Cancel and Edit Fusion Field Service Activities from Service Work Order

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/bsvc-26c/26C-b2b-service-wn-f46524.htm)

You can now reschedule, cancel, and edit Fusion Field Service activities associated with Fusion Field Service work orders, enabling more flexible management of all field service activities tied to the work defined in the work order.

• **Reschedule** — Uses the existing scheduling framework to now support scheduling at the individual activity level for activities associated with the work order.
• **Cancel** — Allows cancellation of a specific associated activity without canceling the entire work order, which may contain multiple activities.
• **Edit** — Opens the selected Fusion Field Service activity directly in Fusion Field Service, providing full access to manage and update the activity details.

This new functionality improves operational flexibility and efficiency by allowing service organizations to manage individual Fusion Field Service activities directly from the Fusion Service work order without impacting the entire work order lifecycle.

• **Improved Scheduling Flexibility** — Service teams can reschedule individual activities independently, enabling faster adaptation to technician availability, customer requests, changing priorities, or unexpected delays without disrupting the broader work order.
• **Reduced Operational Disruption** — Specific activities can now be canceled without canceling the entire work order, helping organizations avoid unnecessary rework and maintain continuity for remaining planned activities.
• **Streamlined Activity Management** — Direct access to edit activities in Fusion Field Service simplifies updates and reduces navigation between systems, improving dispatcher and coordinator productivity.
• **Better Resource Utilization** — Activity-level management helps optimize technician schedules and resource allocation by enabling more precise control over field service execution.
• **Enhanced Customer Experience** — Faster adjustments to appointments and service activities improve responsiveness and help ensure customer commitments are met more efficiently.
• **Greater Visibility and Control** — Organizations gain more granular control over multi-activity work orders, supporting more effective management of complex service scenarios involving multiple visits or technicians.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

The new actions are available in the **Fusion Field Service Activities** section of the Fusion Service work order details page through a new **Actions** column.

Available actions include:

• **Reschedule**
• **Cancel**
• **Edit**

These actions are displayed based on the user’s assigned privileges and permission groups. If a user does not have the required access for a specific action, that action will appear disabled and cannot be executed.

## 🔐 Access Requirements

To perform these actions on Fusion Field Service activities associated with Fusion Service work orders, users must have the following permissions and privileges:

• **View Activities**
• *Read Field Service Activity REST Resource* permission group
• **Cancel Activities**
• *Cancel Field Service Activity REST Resource* permission group
• **Reschedule Activities**
• *Move Field Service Activity REST Resource* permission group
• *Update Field Service Activity REST Resource* permission group
• **Edit Activities**
• *Access Field Service Mobile App* privilege
• *Manage Field Service Activities* privilege

For the **Edit** action, users must also exist as users in Fusion Field Service. When opening an activity, the page and functionality available to the user are determined by their assigned Fusion Field Service user type and associated permissions.

## 📚 Key Resources

Implementing Fusion Field Service Work Orders

Getting Started with Oracle Fusion Field Service in Fusion Applications

Oracle Fusion Field Service 26B What's New

---
*Oracle Cloud Readiness · 26C · SERVICE · Service Center*