[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Manufacturing](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/manufacturing.md)

# Use Additional Parameters for the Process Item Structure Changes to Work Definitions Scheduled Process and Purge Item Structure Events

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/mfg26c/26C-mfg-wn-f44527.htm)

Today, you can optionally run the Process Item Structure Changes to Work Definitions scheduled process to synchronize item structure component changes in the impacted work definitions. Depending on the change, the scheduled process can either directly synchronize the change in existing versions of the impacted work definitions, or send a notification for the user to review and take action.

Before this update, the scheduled process only used the Organization parameter to filter the item structure changes to process. When you ran the scheduled process for the first time, it could slow down system performance.

This update adds the following parameters that provide additional guardrails against scenarios where historical structure changes are also processed:

• **Process Structure Events Created in Past Days:** Set to 90. Prevents item structure events older than 90 days from being processed.
• **Structure Change Notifications:** You can choose if you want structure change notifications to be sent for changes that can’t be automatically synchronized.

Additional Parameters for Process Item Structure Changes to Work Definitions

Additionally, this update also introduces a purge mechanism to delete item structure events. You can use the new scheduled process Purge Item Structure Events Affecting Work Definitions to delete item structure events.

• By default, the scheduled process only purges item structure events that were processed.
• You have the option to purge unprocessed item structure events with a creation date older than 90 days.
• Unprocessed item structure events created in the past 90 days can't be purged.

This behavior aligns with the updated Process Item Structure Changes to Work Definitions scheduled process, which only processes item structure events for the past 90 days.

Purge Item Structure Events Affecting Work Definitions Scheduled Process

The additional parameters in the Process Item Structure Changes to Work Definitions scheduled process and the new  Purge Item Structure Events Affecting Work Definitions scheduled process significantly reduce the likelihood of excessive historical data processing and prevent uncontrolled data growth.

## ⚙️ Steps to Enable and Configure

The Process Item Structure Changes to Work Definitions and Purge Item Structure Events Affecting Work Definitions can be run on demand or scheduled. They can be accessed from either the Work Definition Overview page or the Scheduled Processes work area.

## 💡 Tips and Considerations

Here are recommended best practices:

• If you already schedule the **Process Item Structure Changes to Work Definitions** scheduled process to run regularly: 
  • You don't need to do anything for the **Process Item Structure Changes to Work Definitions** scheduled process. The additional parameters won't impact the existing schedule.
• You should schedule the **Purge Item Structure Events Affecting Work Definitions** to run quarterly and select Yes to purge unprocessed structure events older than 90 days.
• If you don't currently use the **Process Item Structure Changes to Work Definitions** and plan to use it: 
  • You should ensure that historical item structure changes older than 90 days have been synchronized manually to the impacted work definitions.
• You should then run the **Purge Item Structure Events Affecting Work Definitions** scheduled process as soon as possible, and select **Yes**to purge unprocessed structure events older than 90 days.
• Schedule the **Process Item Structure Changes to Work Definitions** scheduled process to run regularly.
• Schedule the **Purge Item Structure Events Affecting Work Definitions** scheduled process to run quarterly, and select **Yes**to purge unprocessed structure events older than 90 days.
• If you don't currently use the **Process Item Structure Changes to Work Definitions** and don't plan to use it: 
  • You don't need to do anything. You can still optionally schedule the **Purge Item Structure Events Affecting Work Definitions** scheduled process to run quarterly and select Yes to purge unprocessed structure events older than 90 days.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Process Item Structure Changes to Work Definitions (WIS_PROCESS_ITEM_STRUCTURE_CHANGES_TO_WORK_DEFINITIONS_PRIV)
• Purge Item Structure Events Impacting Work Definitions (WIS_PURGE_ITEM_STRUCTURE_EVENTS_PRIV)

The first privilege was available prior to this update. The second privilege is new in this update.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: Refer to the Using Manufacturing guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Refer to the Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.
• For more information on Process Item Structure Changes Scheduled Process, refer to Process Item Structure Changes to Work Definitions
• For more information on how you process item structure changes to work definitions, refer to How You Process Item Structure Changes to Work Definitions

---
*Oracle Cloud Readiness · 26C · SCM · Manufacturing*