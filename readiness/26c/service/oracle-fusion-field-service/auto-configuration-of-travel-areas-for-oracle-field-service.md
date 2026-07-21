[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Oracle Fusion Field Service](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/oracle-fusion-field-service.md)

# Auto-Configuration of Travel Areas for Oracle Field Service

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/fscv-26c/26C-fsvc-wn-f49471.htm)

In Update 26B, Oracle Fusion Field Service introduced automatic Travel Area management. At the same time, Oracle Field Service customers were notified that the manual Travel Area configuration was being discontinued. A deprecation banner was shown in Oracle Field Service on the Work Zones and Travel Areas configuration pages to help you prepare for the upcoming change.

**Note**

  This enhancement only applies to **Oracle Field Service** environments. You can verify whether you've Oracle Field Service or Oracle Fusion Field Service, by signing in and checking on the **About** page.

Starting with Update 26C, Oracle Field Service completes this transition. Manual Travel Area configuration is removed from the application. Administrators can continue to configure and maintain Work Zones, but they no longer need to associate Work Zones with Travel Areas.

As part of this update:

• Travel Area configuration is removed from the application.
• The Travel Areas button and the related Travel Area configuration options are removed from the Work Zones area.
• Administrators can create and edit Work Zones without selecting a Travel Area.
• Work Zone import and export no longer require you to maintain Travel Area values.
• For the REST APIs that include Travel Area or Region request parameters, those parameters are now optional.
• Where REST API responses still return Travel Area or Region information, the value is returned as **default**.
• Travel Statistics reports no longer show the Travel Area related **Region Name** and **Region Label** columns.
• Travel Area references are removed from customer-visible areas where manual Travel Area setup was previously shown.
• The temporary deprecation messages shown in 26B are no longer needed and are removed.

For example, before this update, an Oracle Field Service administrator could see the Travel Area configuration options when working with Work Zones. Starting with 26C, those options are removed. The administrator can focus on Work Zone setup without needing to make Travel Area configuration decisions.

This update is not introducing a new Travel Area automation model from scratch. Instead, it completes the rollout of the simplified model that was introduced for Oracle Fusion Field Service in 26B and announced for Oracle Field Service customers as part of the 26B deprecation plan.

## 🎯 Business Benefit

• Reduces configuration complexity because administrators no longer need to create, update, assign, or maintain Travel Areas manually.
• Speeds up implementation as teams can focus on Work Zones, routing, and operational setup without designing a separate Travel Area structure.
• Minimizes setup errors by removing Travel Area decisions that could lead to inconsistent or unnecessary configuration.
• Simplifies ongoing administration with fewer Travel Area fields, buttons, pages, report columns, and configuration steps to manage.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• Review your internal procedures, training materials, reports, and integrations that mention manual Travel Area setup.
• Existing integrations that include Travel Area or Region values continue to work where backward compatibility is supported, but you must not rely on those values to control Travel Area behavior.
• Update custom reports, operational processes, implementation guides, administrator training, and runbooks that previously referenced Travel Area setup.

## 📚 Key Resources

For more information about the 26B Travel Area transition, see these resources:

• Auto Configuration of Travel Areas for Oracle Fusion Field Service
• 26B Deprecation Announcement for Travel Areas

---
*Oracle Cloud Readiness · 26C · SERVICE · Oracle Fusion Field Service*