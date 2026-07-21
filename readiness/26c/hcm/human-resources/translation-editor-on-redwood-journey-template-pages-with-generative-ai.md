[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Human Resources](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/human-resources.md)

# Translation Editor on Redwood Journey Template Pages with Generative AI

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hure-26c/26C-hr-wn-f44442.htm)

You can now use generative AI in the Redwood **Translation Editor** to translate attributes directly on the Redwood journey template pages. You can seamlessly translate translatable attributes, such as the journey template name, description, title, subtitle, task names, and description on the journey template pages. This capability enhances the translation experience by leveraging artificial intelligence to help users generate and refine localized content directly within the editor.

By using this feature, administrators and content authors can quickly produce accurate translations for journey template attributes across multiple languages, reducing the need for manual translation efforts. This helps improve consistency, speed, and quality of localized content while allowing users to review and edit translations before publishing.

Additionally, you can use the generative AI capability for Redwood Translation Editor on these pages:

• Guided Journey
• Task Library
• Task Groups
• Category Security

For example, the Employee Onboarding journey template needs to be translated into Korean language. You click the Employee Onboarding template name and select the Translation Editor value from the More Actions menu.

Translation Editor on Journey Template Page

Select the Korean language for which translations need to be added and click **Edit**.

Select Required Language for Translation

Review the populated journey template attributes and click **Generate**.

Generate Translation for Selected Language

Generative AI translates the attribute values to Korean language. Click **Update**.

Generated Translation for Selected Language

The translated values are added to the table in the Translation Editor.

Updated Translations

Reduces the time and effort required to translate journey template content into multiple languages while improving translation consistency.

## ⚙️ Steps to Enable and Configure

• Ensure that you have access to VB Studio. Instances and workspaces should have been correctly set as well.
• The Generate button isn't displayed by default. To display the button, you need to enable the **Show AI Assist** VB constant on the Journey Templates page. The VB constant is enabled when you set its value to true by using Visual Builder Studio (VB Studio). For more information, see this topic: How do I control the display of a UI element in Visual Builder Studio?
• You need to configure security to use this feature. See the Access Requirements section.
• For more information, see this topic: Translate Journey Template Attributes Using Generative AI

## 💡 Tips and Considerations

• This capability is available only in the Redwood experience.
• The translations that you generate using Gen AI may contain inaccuracies. You need to review them before you update them.

## 🔐 Access Requirements

You need to be granted these privileges and roles:

• Manage Journey (ORA_PER_MANAGE_JOURNEY_TEMPLATE) aggregate privilege to work on journey templates.
• Application Administrator role to access VB Studio.

## 📚 Key Resources

For more information, refer to the Implementing and Using Journeys guide.

Check these resources to understand the prerequisites and steps to create instances and workspaces.

• Set Up Oracle Visual Builder Studio: Learn how to create a VB Studio instance
• Get Started with Oracle Visual Builder Studio: Learn how to create a workspace in VB Studio

---
*Oracle Cloud Readiness · 26C · HCM · Human Resources*