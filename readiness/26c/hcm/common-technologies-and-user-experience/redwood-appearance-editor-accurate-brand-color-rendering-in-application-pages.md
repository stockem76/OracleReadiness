[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Common Technologies and User Experience](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/common-technologies-and-user-experience.md)

# Redwood appearance editor: Accurate brand color rendering in application pages

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/common/26c/common26c/26C-common-wn-f49336.htm)

Previously, Redwood themes using some custom colors displayed lighter or darker variations instead of the exact specified color. Now, Redwood themes apply the exact input primary color, provided the specified custom color meets the color contrast accessibility requirements defined by the Web Content Accessibility Guidelines (WCAG). This color is applied to supported theming surfaces including page headers and supported areas in Oracle Application Development Framework.

Here's an illustration that shows the difference in color application between the previous release and this release.

You can now display your exact brand color in Fusion Applications, provided it meets the contrast requirements.

## ⚙️ Steps to Enable and Configure

If you have an existing theme with the custom color that meets the contrast requirements, your color isn't automatically reflected unless you save or apply the theme. To apply the Redwood theme with your brand color:

1. In Sandboxes, create a sandbox or enter an existing one. Make sure the sandbox has the Appearance tool. Don't include spaces or special characters in the sandbox name.
2. From the sandbox **Tools** menu, select **Appearance**.
3. Create a Redwood theme with your brand color. Or, if you already have one, save or apply the theme.
4. Publish the sandbox.

**Note:**Your brand color is applied accurately only if it meets the contrast requirements, else you'll see darker or lighter variations of the color.

---
*Oracle Cloud Readiness · 26C · HCM · Common Technologies and User Experience*