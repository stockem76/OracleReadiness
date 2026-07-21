[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# Redwood: Automatically Calculate and Review PAR-Level Values Before Updating Current Values

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f46487.htm)

Hospitals and healthcare providers rely on accurate PAR (Periodic Automatic Replenishment) levels to ensure critical supplies are consistently available while avoiding overstocking and waste. However, determining optimal PAR levels is often a manual, time-intensive process that may not fully account for varying demand patterns, leading to inefficiencies in supply management and potential risks to patient care. In update 26A, we introduced the ability to upload externally calculated PAR values, allowing you to review and manually adjust them if needed before publishing the updated values. You can now automatically calculate optimal PAR levels by leveraging historical replenishment data to generate intelligent recommendations. Users can review and update these system-generated recommendations before publishing them to Oracle Fusion Cloud Inventory Management, ensuring both data-driven accuracy and operational control.

Now in release 26C, policy profiles have been extended to support Inventory PAR replenishment in addition to min-max planning. Suggested PAR levels are calculated based on the prerequisite setup in the Functional Setup Manager. New Redwood pages have been added to allow you to configure specific PAR replenishment attributes to maintain optimal PAR levels. The new Redwood pages are:

• Default Classification
• Policy Profiles
• Policy Profile Assignments

You can calculate PAR levels by submitting the **Calculate PAR Levels** scheduled process from the PAR Levels page. Once submitted, a confirmation message is displayed. You can monitor the process by navigating to the Action Status tab. Once the process has completed, the PAR levels will be updated accordingly based on historical data. You can optionally submit the **Calculate Policy Parameters for Min-Max Planning and PAR** process from the Scheduled Processes work area.

Calculate PAR Levels

In the event you need to override the **Suggested PAR Level** and **Suggested PAR** maximum quantities, you can edit the row and enter the **Override PAR Level** and **Override PAR Maximum** quantities. This provides you with the flexibility to update the suggested PAR levels when required. Once you have reviewed the calculated PAR levels, you have the option to either publish the values or retain the current values. When you publish the calculated or suggested PAR levels, the corresponding PAR levels will be updated at the item subinventory and item locator levels on the Configure Subinventories page.

Override PAR Levels

This example explains how the PAR levels and PAR maximum levels are computed.

• Input: 
  • PAR Time Period = 30 days
• Number of Deliveries per Time Period = 4
• Using the current calculation method, the average daily demand and safety stock will be calculated: 
  • Calculated Average Daily Demand = 3.33
• Calculated Safety Stock = 40
• Average Inventory Usage in the time period is calculated as: Calculated Average Daily Demand * PAR Time Period 
  • Average Inventory Usage in the Time Period is 3.33*30=100
• PAR Level is calculated as: (Average Inventory Usage in the time period + Safety Stock) / Number of Deliveries per Time Period 
  • PAR Level is (100+40)/4=35
• PAR Maximum Quantity is calculated as: Maximum Quantity Days of Cover * Calculated Average Daily Demand 
  • If the Maximum Quantity Days of Cover is defined as 14 days, then the PAR Maximum Quantity is 14*3.33=47

This feature streamlines replenishment, improves supply availability, and enables healthcare organizations to maintain optimal inventory levels with greater confidence and efficiency.

## ⚙️ Steps to Enable and Configure

When setting up PAR replenishment and min-max planning for Oracle Inventory Management, you can create classifications to categorize your items. You associate categories with similar item attributes with a classification. Categorizing items with similar attributes enables you to specify the policies for computing the PAR and min-max quantities efficiently.

**Create Default Classification Group**

1. In the Setup and Maintenance work area, go to the **Default****Classification Group** task: 
  • Offering: Manufacturing and Supply Chain Materials Management
• Functional Area: Inventory Management
• Task: Default Classification Group
2. On the Default Classification Group page, in the Classifications section, click the **Add (+)** button to create a new classification.
3. In the New classification panel drawer, specify the following: 
  • Enter a classification and description
• Enter criteria details
4. Click **Create**.

**Create Policy Profiles**

1. In the Setup and Maintenance work area, go to the **Policy Profiles** task: 
  • Offering: Manufacturing and Supply Chain Materials Management
• Functional Area: Inventory Management
• Task: Policy Profiles
2. On the Policy Profiles page, click the **Add (+)** icon.
3. On the New Policy Profile page: 
  • Enter a policy profile name and description
• Enter replenishment policy details
• Enter minimum quantity details
• Enter maximum quantity details
4. Click **Create**.

**Create Policy Profile Assignments**

1. In the Setup and Maintenance work area, go to the **Policy Profile Assignments** task: 
  • Offering: Manufacturing and Supply Chain Materials Management
• Functional Area: Inventory Management
• Task: Policy Profile Assignments
2. On the Policy Profile Assignments page, click the **Add (+)** icon.
3. In the New policy profile assignment panel drawer: 
  • Select a classification
• Select an organization
• Select a subinventory
• Select a policy profile
• Set the **Calculate Policy Parameters**option to**Yes**or**No**
4. Click **Create**.

**Nudges Overview**

A nudge is a reminder sent to a worker to take a specific action on a certain event. Managers and employees can receive nudges for any overdue or pending tasks pertaining to events. Inventory replenishment value calculation is one such event where nudges can be configured to send reminders. You can configure nudges to send reminders through email or SMS.

Navigate to the Nudge Plans page by selecting the **Nudge Configuration** task from the quick actions.

**Create a New Nudge Plan**

1. On the Nudge Plans page, click **Create** to add a new plan.
2. In the New nudge plan drawer:   
  • Enter the nudge plan name
• Enter the nudge plan description
• Select the start date and end date
• Select the subscriber inventory
• Select the **Min-Max and PAR adjustment** type
3. Click **Create Draft**.
4. After the nudge is in draft state, select the nudge and click the **Add**button to create a new nudge. 
  • Select the **Min-Max and PAR adjustment** module
• Enter the organization for which you want to retrieve nudges when cross-dock opportunities exist
5. Click **Save**.

**Add Recipient Groups**

1. On the Inventory Replenishment page, click the Advanced tab of the draft nudge plan.
2. In the Recipient Groups section, click **Add** to create the recipient groups that will receive notifications for nudges in the nudge plan.
3. In the Users section, click **Add** to add users to the recipient group.
4. Click **Save**.

**Configure Notification Channel and Recipient**

1. On the New Nudge page, click the nudge name link to open its details.
2. In the Channels section, click **Add** to create a new channel.
3. On the New Channel page, choose whether to send notifications through email, SMS, or both, and select the recipient group to receive the notification.
4. For email notifications, you can personalize the subject and body using user-defined content.
5. After the nudge plan is configured, click **Activate** to enable the nudge plan.

## 💡 Tips and Considerations

• Historical receipt transactions at the subinventory level are considered for computing the PAR level and PAR maximum level.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains this privilege can access this feature:

• Review Min-Max Values and PAR Levels (INV_REVIEW_MIN_MAX_VALUES_PAR_LEVELS_PRIV)

This privilege was available prior to this update.

To set up this feature, you'll need a configured job role that contains this existing privilege:

• Manage Min-Max Planning Policies (INV_MANAGE_MIN_MAX_PLANNING_POLICIES_PRIV)

This privilege was available prior to this update.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: Using Inventory Management guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Security Reference for Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*