[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Supply Planning](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/supply-planning.md)

# Redwood: Deep Links to Planning Pages and Visualizations with Context

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/scp26c/26C-sc-planning-wn-f45843.htm)

You can now navigate between planning pages using deep links that preserve context such as plan, page, page group, visualization, and filter details. It improves analysis efficiency by directly accessing relevant pages or visualizations with up to five filter context values applied. This also supports better exception and resource overload analysis by linking related plan outputs across different plan types or applications.

When navigating to the Redwood Supply Chain Planning, you can provide either the name or the corresponding ID for the following parameters:

• Plan Name or Plan ID
• Page Name or Page ID
• Page Group Name or Page Group ID
• Visualization Name or Visualization ID
• Context Name or Context ID

If you don’t specify a page, page group, or visualization as a parameter, the last used page group opens by default. If you specify a page or visualization along with a page group, the specified page group is opened with the provided page or visualization set as the active landing tab.

A deep link URL for this feature consists of two parts:

• Base URL: Provides the host information.
• Object key values: The object key values consist of plan and the following parameters:
• startPlan or startPlanId
• startPage or startPageId
• startPageGroup or startPageGroupId
• startViz or startVizId
• startLevel or startLevelId and startLevelMember or startLevelMemberId

For example:

https://< hostname>/fscmUI/redwood/supply-chain-planning/?startPageGroupId=5007&startPlanId=300100652134040&startVizId=1001&startLevel=Organization&startLevelMember=M1&startLevel1=Item&startLevelMember1=VKO-Laptop

Spaces between parameter names are accepted by the deep link URL.

For example:

https:// < hostname>//fscmUI/redwood/supply-chain-planning/?startPageGroupId=5007&startPlanId=300100652134040&startVizId=1001 &startLevel=Organization&startLevelMember=Boston Manufacturing

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

It’s recommended to use **parameter or object IDs**instead of names, as IDs remain consistent even if the corresponding parameter or object is renamed.

  You can retrieve these parameters or object IDs by querying the relevant database tables for the specific parameters.

• Plan Id: msc_plan_definitions
• Page or Page group: msc_metadata_objects_vl
• Visualization: msc_table_graph_options_vl & msc_workarea_task_flows_vl
• Context: msc_entity tables

You can provide up to 5 context values in the deep link URL.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Monitor Demand and Supply Planning Work Area (MSC_MONITOR_DEMAND_AND_SUPPLY_PLANNING_WORK_AREA_PRIV)
• Monitor Supply Planning Work Area (MSC_MONITOR_SUPPLY_PLANNING_WORK_AREA_PRIV)

This privilege was available prior to this update.

---
*Oracle Cloud Readiness · 26C · SCM · Supply Planning*