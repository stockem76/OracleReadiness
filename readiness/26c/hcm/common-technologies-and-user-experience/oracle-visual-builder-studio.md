[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Common Technologies and User Experience](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/common-technologies-and-user-experience.md)

# Oracle Visual Builder Studio

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/common/26c/common26c/26C-common-wn-f50157.htm)

Here are some key things you can now do to extend your application pages using Visual Builder Studio:

• Reorder Fields: Support labels for concrete objects

Allows Oracle Fusion Cloud Applications Extension developers to specify arbitrary labels for region tree items in the Reorder Fields panel. This feature provides an enhancement to the Reorder Fields panel. If multiple layouts share the same concrete business object (BO), a region tree item is created that contains those multiple layout tree items. The label of that region tree item can now be configured using the labelHint property in the BO's data description.

• Reorder Fields: Revert to factory ordering

Allows customers using the Reorder Fields panel in Express mode to reorder certain fields and revert their changes to the factory ordering.

• DT-driven dynamic list of values (LOV) for $fields

Allows Oracle Fusion Cloud Applications Extension developers to specify how to fetch an LOV for a given business object field in Design Time's (DT) Business Rules Editors without affecting runtime behavior of that field. In 24B, Visual Builder Designer provided a way for developers to configure dynamic LOV for `$fields`. This involved defining an LOV service data provider (SDP), then configure client metadata augmentation on a target field to use that service for fetching LOVs. However, augmenting the client metadata using the dataProvider attribute defined by the dynamic components directly impacts the runtime LOV behavior of that field as well. This is undesirable most of the time and the solution is to provide DT-only metadata when augmenting the target field to dynamically fetch LOVs. Only the Visual Builder Designer will recognize and support this metadata, while the dynamicui runtime will ignore them.

• Business Rules (BR) Editor: Remove context value from context LOV menu

Allows Oracle Fusion Cloud Applications Extension developers or customers to remove a context value from a context LOV dropdown. The BR editor now supports removing a context value from the context LOV dropdown. This is done by selecting the Remove option in the assignment legislative (DDF) and customer-defined (DFF) subtype.

• Square bracket notation for overlay fields

Overlay fields that contain special characters, spaces, or dots, are now written with the square bracket notation.

After upgrading Visual Builder Design Time (VBDT) to 26.07, whenever a user enters the Business Rules Editor, a check is run to determine if there are any overlay fields that need to be rewritten to the square bracket notation.

• Enable OIC or OPA backends creation in Extensions and allow OIC backends to create a local server with variables

Allows extension developers and customers to create Oracle Integration Cloud (OIC) and OCI Process Automation (OPA) backends with the “Create backend” flow.

In Visual Apps, users have a unique experience with out-of-the box backends, like “Integrations” and “Process Automation”. This is now available in Extensions.

In OIC backends, you can create a local server with variables that is needed for OIC Gen 3 to handle redirects to the design URL.

• Business Objects (BO)

   Allows extended string lengths up to 32K and is now aligned with Oracle DB extended VARCHAR2 capabilities. Customers modeling enterprise data with long text attributes, such as rich descriptions, payload fragments, larger notes, and integration content, can store and process these values in BOs without premature truncation or redesigning of schemas around the previous 4K limits.
• Rule-based Flow Properties

   Allows Oracle Fusion Cloud Applications extension customers to create rule-based properties for factory dependency pages at the flow level. In some pages, you can now use the Flow Properties editor to create rules and conditions to set the value of page properties. For Advanced mode, see Set Property Values Using Rules; for Express mode, see Set Property Values Using Rules.
• New `oj-c components`

Here are new`oj-c components`:

1. In Early access:

   a. `oj-c-picto-chart`

   b. `oj-c-picto-chart-item`
2. Superseding:

   a. `oj-c-accordion-item-singlej-c-picto-chart`

   b. `oj-c-accordion-item-multiplej-c-picto-chart-item`

These legacy JET components have changed their status to maintenance:

1. `oj-accordion`
2. `oj-collapsible`
3. `oj-combobox-one` (superseded by `oj-c-select-single`)

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · HCM · Common Technologies and User Experience*