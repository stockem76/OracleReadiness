[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Redwood: Enable HR Administrators to Publish Organization Goals on Behalf of Executive Leaders

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f43921.htm)

From this release, as administrators you can enable HR specialists to create performance and development goals on behalf of organization leaders. When HR specialists add a goal for a person who has the privileges to create organization goals from their Goals Center page, they’ll see a switch that allows them to publish the goal for that person’s organization. They need to set this switch to **On** position to publish the goal for persons in that organization leader’s hierarchy.

New Goal page

When members of the organization leader’s hierarchy view organization goals on the Explore tab or in the Suggested goals panel, they can see the goal as published by their organization leader and not the HR specialist.

Organization goals on Explore tab

## 🎯 Business Benefit

Reduce the workload of organization leaders by enabling HR specialists to assign goals on their behalf.

## ⚙️ Steps to Enable and Configure

To enable Redwood Goals Center, you need to enable the profile options indicated in the table.

Profile Option Code | Profile Option Display Name | Value
ORA_HCM_VBCS_PWA_ENABLED | Enable VBCS Progressive Web Application User Interface | Y
ORA_HRA_PERFORMANCE_DOCUMENTS_AND_GOALS_REDWOOD_ENABLED | Enable Redwood Performance Documents and Goals Center | Yes

**NOTE**: The Performance Document, Check-in, and Goals Center features are closely connected. So, the Redwood version of these pages can all be enabled or disabled only using the common ORA_HRA_PERFORMANCE_DOCUMENTS_AND_GOALS_REDWOOD_ENABLED profile option. These features can't be enabled individually.

For more information, see How do I enable a profile option?.

## 🔐 Access Requirements

To enable HR specialists to publish organization goals on behalf of an organization leader, you need to do these steps:

1. Go to **Tools** > **Security Console**.
2. Create a custom role for allowing HR specialists to create organization goals for others.
3. Select the category as **HCM-Job Roles**.
4. Enable permission groups.
5. On the **Role Hierarchy** train stop, add the **Create Organization Performance Goal for Others** aggregate privilege.
6. On the **Users** train stop, assign this custom role to the users who you want to create organization goals for business leaders.
7. Save your changes.
8. Go to the **Setup and Maintenance** work area.
9. Search for and open the **Manage Person Security Profiles** task.
10. Create a new person security profile.
11. Give it a suitable name.
12. Secure it by one of these attributes depending on the requirement:

• Manager hierarchy
• Department
• Business unit
• Person type
• Custom criteria
• Submit your changes.

1. In the **Setup and Maintenance** work area, search for the **Manage Data Roles and Security Profiles** task.
2. Edit the custom role that you created to allow HR specialists to create organization goals for others.
3. On the **Security Criteria** train stop, select the person security profile you created earlier.
4. Submit your changes.
5. Go to **Tools** > **Security Console**.
6. Select the **Roles** tab.
7. Edit the custom role that you created to allow HR specialists to create organization goals for others.
8. Verify that the role has the data security policy and person security policy that you created.
9. Select the **Users** tab.
10. Verify that the intended users are assigned the **Create Organization Performance Goal for Others** aggregate privilege.

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*