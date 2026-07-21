[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Order Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/order-management.md)

# Redwood: Use Transactional Item Attributes in Configurator Rules

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/order26c/26C-order-mgmt-wn-f49413.htm)

Use item class transactional attributes to influence rule evaluation during a configuration session. These attributes provide runtime values that you can reference in rule conditions to dynamically control the model for example, automatically select or exclude options and enforce constraints based on the transactional context.

Realize these benefits:

• **Context-Aware Configurations:**Drive rule behavior based on live transactional values, ensuring the configured product reflects the actual order context.
• **Automatic Option Control:**Automatically select or exclude configuration options based on transactional attributes, reducing manual effort and configuration errors.
• **Dynamic Constraint Enforcement:**Apply constraints that adapt in real time to the transactional environment, improving accuracy and compliance.

Try it:

1. **Define Transactional Attributes on an Item Class**

    Navigate to Product Management and add or verify the transactional attributes defined on the relevant item class.
2. **Open the Configurator Model**

    From Product Management, open the ATO or PTO configurator model you want to update.
3. **Create or Edit a Rule**

    Add a new rule or edit an existing formula-based configurator rule from the **Structures**tab of the model.
4. **Reference a Transactional Attribute in the Configurator Rule**

    In the rule condition, select the transactional attribute as the operand by dragging and dropping it into the rule text area. The attribute will be resolved at runtime using the current transactional context. Specify the selection, exclusion, or constraint that the rule should enforce when the condition is met.
5. **Test the Rule in a Configuration Session**

    Initiate a test configuration session and verify that the rule evaluates correctly based on the transactional attribute values present in that session.

The following screenshot shows a configurator rule referencing a transactional item attribute in the rule condition.

Transactional Attribute Referenced in a Configurator Formula Rule

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

**Inactive Transactional Attributes:** If a transactional attribute that participates in a rule is set to inactive and the rule definition isn't updated to account for the inactivation, an error is displayed at runtime that identifies the affected rule so an administrator can take corrective action.

**Transactional Attributes in****Formula Rules:** The **contributesTo**operator isn't currently supported with transactional attributes in formula-based configurator rules.

## 🔐 Access Requirements

Users who are assigned a job role that contains these duty roles and privileges can access this feature:

• Configurator privileges or duty roles: 
  • Configurator privileges: 
    • Manage Configurator Rules (CZ_MANAGE_RULES_PRIV)
• Test Configurator Model (CZ_TEST_MODEL_PRIV)
• Access Configurator Runtime (CZ_CONFIGURATOR_RUNTIME_ACCESS_PRIV)
• Access HCM Common Components (HRC_ACCESS_HCM_COMMON_COMPONENTS_PRIV)
• Manage HCM Rules (HRC_MANAGE_HCM_RULES_PRIV)
• Configurator duties: 
    • Redwood Configurator Manager (ORA_CZ_REDWOOD_MANAGER_DUTY)
• Redwood Configurator Manager (ORA_REDWOOD_MANAGER_DUTY_HCM) – For access to the Rule Builder details
• Redwood Configurator Reviewing (ORA_CZ_REDWOOD_REVIEWING_DUTY) – Optional for read-only access to the Configurator Rule details
• Redwood Configurator Reviewing (ORA_CZ_REDWOOD_REVIEWING_DUTY_HCM) – Optional for read-only access to the Rule Builder detail
• Duties and privileges for Product Management: 
  • View Item Redwood Items (EGP_VIEW_REDWOOD_ITEM_PRIV)
• View Item Redwood Attachments (EGP_VIEW_REDWOOD_ITEM_ATTACHMENT_PRIV)
• View Item Redwood Associations (EGP_VIEW_REDWOOD_ITEM_ASSOCIATION_PRIV)
• View Item Redwood Structures (EGP_VIEW_REDWOOD_ITEM_STRUCTURE_PRIV)
• View Item Redwood Changes (EGP_VIEW_REDWOOD_ITEM_CHANGE_PRIV)
• View Item Redwood Item Categories (EGP_VIEW_REDWOOD_ITEM_CATEGORIES_PRIV)
• View Item Redwood Relationships (EGP_VIEW_REDWOOD_ITEM_RELATIONSHIP_PRIV)
• View Item Redwood Quality (EGP_VIEW_REDWOOD_ITEM_QUALITY_PRIV)
• Supply Chain Common View Web Service (ORA_RCS_SCM_COMMON_VIEW_WEB_SERVICE_DUTY)
• Enter Trading Community Organization Information (HZ_ENTER_TRADING_COMMUNITY_ORGANIZATION_INFORMATION_PRIV)
• Get Failure Condition Event Codes (MNT_GET_FAILURE_CONDITION_EVENT_CODE_BY_SERVICE_PRIV)
• Get Item Attribute Control REST (EGP_ITEM_ATTRIBUTE_CONTROL_READ_PRIV)
• Get Item Lifecycle Phases Read Rest (EGP_ITEM_LIFECYCLE_PHASES_READ_REST_PRIV)
• Get Item Status REST (EGP_ITEM_STATUSES_READ_PRIV)
• Get New Item Request Rest (EGI_NEW_ITEM_REQUEST_REST_PRIV)
• Get Template REST (EGP_TEMPLATE_READ_PRIV)
• Manage Material Planner (MSP_MANAGE_MATERIAL_PLANNER_PRIV)
• Manage Subscription Setup (OSS_MANAGE_SUBSCRIPTION_SETUP_PRIV)
• Remove Trading Community Organization (HZ_REMOVE_TRADING_COMMUNITY_ORGANIZATION_PRIV)
• Set Up Receivables Payment Terms (AR_SET_UP_RECEIVABLES_PAYMENT_TERM_PRIV)
• Update Trading Community Organization (HZ_UPDATE_TRADING_COMMUNITY_ORGANIZATION_PRIV)
• Verify Tax Configuration (ZX_VERIFY_TAX_CONFIGURATION_PRIV)
• View Procurement Buyers List of Values using REST Service (PO_VIEW_BUYER_LOV_REST_SERVICE_PRIV)
• View Purchasing Hazard Classes List of Values using REST Service (PO_VIEW_HAZARD_CLASSES_LOV_REST_SERVICE_PRIV)
• View Purchasing UN Numbers List of Values using REST Service (PO_VIEW_UNNUMBER_LOV_REST_SERVICE_PRIV)
• View Trading Community Organization (HZ_VIEW_TRADING_COMMUNITY_ORGANIZATION_PRIV)
• View Trading Community Person (HZ_VIEW_TRADING_COMMUNITY_PERSON_PRIV)
• Manage Item Redwood Items (EGP_MANAGE_REDWOOD_ITEM_PRIV)
• Manage Item Redwood Attachments (EGP_MANAGE_REDWOOD_ITEM_ATTACHMENT_PRIV)
• Manage Item Redwood Associations (EGP_MANAGE_REDWOOD_ITEM_ASSOCIATION_PRIV)
• Manage Item Redwood Item Categories (EGP_MANAGE_REDWOOD_ITEM_CATEGORY_PRIV)
• Manage Item Redwood Relationships (EGP_MANAGE_REDWOOD_ITEM_RELATIONSHIP_PRIV)
• Manage Item Redwood Structures (EGP_MANAGE_REDWOOD_ITEM_STRUCTURE_PRIV)
• Get New Item Request Rest (EGI_NEW_ITEM_REQUEST_REST_PRIV)
• Manage Item Status REST (EGP_ITEM_STATUSES_PRIV)

These privileges were available prior to this update.

---
*Oracle Cloud Readiness · 26C · SCM · Order Management*