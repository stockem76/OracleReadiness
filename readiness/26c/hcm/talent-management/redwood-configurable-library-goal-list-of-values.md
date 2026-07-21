[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Redwood: Configurable Library Goal List of Values

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f49993.htm)

As administrators, configure the attributes that display in the performance and development library goals list of values so that only the search attributes that are relevant to your organization appear when employees, managers, or HR specialists search for library goals.

  By default, these attributes are displayed when you search performance library goals:

• Goal name
• Category
• Subtype

By default, these attributes are displayed when you search development library goals:

• Goal name
• Category

## 🎯 Business Benefit

Leverage this feature and enable employees, managers, and HR specialists to search and find the required library goals easily.

## ⚙️ Steps to Enable and Configure

To enable Redwood Goals Center, you need to enable the profile options indicated in the table.

Profile Option Code | Profile Option Display Name | Value
ORA_HCM_VBCS_PWA_ENABLED | Enable VBCS Progressive Web Application User Interface | Y
ORA_HRA_PERFORMANCE_DOCUMENTS_AND_GOALS_REDWOOD_ENABLED | Enable Redwood Performance Documents and Goals Center | Yes

**NOTE**: The Performance Document, Check-in, and Goals Center features are closely connected. So, the Redwood version of these pages can all be enabled or disabled only using the common ORA_HRA_PERFORMANCE_DOCUMENTS_AND_GOALS_REDWOOD_ENABLED profile option. These features can't be enabled individually.

For more information, see How do I enable a profile option?.

To configure the library goal list of values:

1. Go to **Configuration** > **Sandboxes**.
2. Select and enter a sandbox that has HCM Experience Design Studio enabled.
3. Select **Tools** > **HCM Experience Design Studio** > **Search Configuration**.
4. Configure performance library goal list of values:
1. Select the **Performance Goal Library** list of values.
2. Select the search and display fields. You can select goal name, business unit, department, legal employer, and job family as a search and display field. Reorder them if needed.
3. Select fields only for search. You can select business unit, department, legal employer, and job family as a search field.
4. Preview your changes.
5. Save your changes.
5. Configure development library goal list of values:
1. Select the **Development Goal Library** list of values.
2. Select the search and display fields. You can select goal name, business unit, department, legal employer, and job family as a search and display field. Reorder them if needed.
3. Select fields only for search. You can select business unit, department, legal employer, and job family as a search field.
4. Preview your changes.
5. Save your changes.
6. Publish your changes.

Edit these pages of both performance and development goals in Visual Builder Studio and set the **Show Library Goal List of Values** page property to true:

• New Goal
• New Goal Plan
• Goal Plan Details
• New Mass Assignment or Mass Share Goals Process (performance goals)
• Setup of Performance Goals Mass Assignment or Mass Share Goals Process Details
• New Mass Assignment Goals Process (development goals)
• Setup of Development Goals Mass Assignment Process Details

For more information on how to do this, see How do I control the display of a UI element in Visual Builder Studio?.

## 📚 Key Resources

For more information on extending Redwood pages in HCM, refer to this guide on the Oracle Help Center:

• Extending Redwood Applications for HCM and SCM Using Visual Builder Studio

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*