[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Oracle Fusion Field Service](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/oracle-fusion-field-service.md)

# Navigation to MyRoute from Plugins

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/fscv-26c/26C-fsvc-wn-f49355.htm)

**Oracle Fusion Field Service 26C** introduces an enhancement that provides greater flexibility for plugin-based completion workflows by enabling mobile workers to return directly to **MyRoute** after an activity is completed. The Plugin API `close`method has been enhanced to support **MyRoute** as a value for the `backScreen`parameter. When this option is used, the mobile application automatically returns the worker to MyRoute at the end of the plugin workflow. This helps streamline navigation, improve workflow continuity, and allow mobile workers to quickly continue their day from the primary day-of-work view. This capability is supported in both online and offline mobile scenarios, so mobile workers can be returned to the appropriate route view even when working without network connectivity.

**How it works?**

When a plugin invokes the Plugin API close method with backScreen set to my_route, the following behavior occurs:

1. The plugin closes.
2. The mobile application navigates the worker to **MyRoute**.
3. The worker can immediately continue their day by reviewing the route, starting travel, or opening the next activity. This reduces unnecessary navigation and helps workers stay focused on their next task after completing a plugin-based workflow.

**Note:** If your environment is configured to use **Activity List** as the **Field Resource Landing Page**, then a plugin call to close with backScreen set to my_route navigates the mobile worker to the **Activity List** page instead.

**Plugin Developer Usage**

• Call the Plugin API **Close**method at the end of the plugin workflow.
• Set the **backScreen**parameter to **"my_route"**.

**Request Example**

{
    "apiVersion": 1,
    "method": "close",
    "backScreen": "my_route"
}

This returns the mobile worker to MyRoute, or to the configured field resource landing page when Activity List is set as the landing experience.

## 🎯 Business Benefit

This enhancement helps improve the mobile worker experience by reducing unnecessary navigation after completing plugin-based workflows.

Key benefits include:

• **Streamlined post-completion navigation:** Mobile workers can move directly from plugin-based activity completion to MyRoute.
• **Improved mobile worker efficiency:** Fewer taps are needed to move from activity completion to the next action, such as reviewing the route, starting travel, or opening the next activity.
• **More consistent mobile experience:** Plugin-enabled workflows can now follow the same expected navigation pattern as other completion flows, creating a familiar and predictable user experience.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

This enhancement is well suited for plugin-enabled activity completion workflows where workers need to quickly return to their route and take the appropriate next action.

---
*Oracle Cloud Readiness · 26C · SERVICE · Oracle Fusion Field Service*