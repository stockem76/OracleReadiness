[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Oracle Fusion Field Service](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/oracle-fusion-field-service.md)

# DKIM-compliant reply addresses in message scenario email steps

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/fscv-26c/26C-fsvc-wn-f49608.htm)

Starting in 26C, Oracle Field Service validates the Reply address domain used in the Email steps of message scenarios to help ensure DKIM-compliant email delivery.

A Reply address is considered valid when:

• its domain is either the default Oracle Field Service domain, such as fs.ocs.oraclecloud.com, or
• a customer-configured domain with active DKIM configuration for the subscription.

For new Email steps, the Reply address is automatically set to `noreply@fs.ocs.oraclecloud.com.`

In non-Fusion Field Service environments, users can change the Reply address, but Oracle Field Service prevents the message scenario from being saved if the selected or entered domain is not DKIM-enabled. In Oracle Fusion Field Service environments, the Reply address is read-only and remains fixed to the default value.

To help users correct the existing configurations, Oracle Field Service identifies message scenarios that require attention, for example:

• A warning appears on the configuration page when one or more message scenarios contain Email steps with a non-DKIM-enabled Reply address domain.
• The message scenarios list marks only the scenarios that contain at least one affected Email step.
• The scenario steps list marks each affected Email step.
• When users open an affected Email step for modification, the Reply address field displays an error so they can update it.

This validation applies only to **Email steps in message scenarios**. Other message scenario step types are not evaluated by this rule.

## 🎯 Business Benefit

This feature improves outbound email reliability by preventing message scenarios from using the Reply address domains that are not authorized for the subscription.

Key benefits include:

• Reduces email delivery failures caused by Reply address domains that are not DKIM-enabled.
• Helps users quickly identify and correct affected message scenarios.
• Provides clear warnings and validation messages that guide users to the required action.
• Ensures consistent enforcement through both user interface validation and server-side validation.
• Prevents users from saving message scenarios with invalid Reply address configurations.

## ⚙️ Steps to Enable and Configure

This feature is enabled automatically through the **Multitenant Service deployment**. It is applied to all applicable environments at the service level, so users do not need to upgrade individual environments or perform any customer-side enablement.

Users should review their message scenarios and update any Email steps that use a Reply address domain that is not DKIM-enabled for the subscription.

To resolve affected message scenarios:

1. Open the **Message Scenarios** configuration page.
2. Review the scenarios marked with the DKIM Reply address warning.
3. Open an affected scenario.
4. Review the Email steps marked with the warning.
5. Edit the **Reply** **address** in each affected Email step.
6. Replace the **Reply address** with either:   
  • `noreply@fs.ocs.oraclecloud.com`, or
• an address from a domain that is DKIM-enabled for the subscription.
7. Save the message scenario.

To use a customer-managed domain in the Reply address, the domain must first be registered and DKIM-enabled, as described in Register Your Domain to Enable DKIM.

## 💡 Tips and Considerations

• This validation applies only to Email steps in message scenarios. Other step types are not evaluated, marked, or blocked by this rule.
• Existing message scenarios remain available for review. If a scenario includes an Email step with a Reply address domain that is not DKIM-enabled, the scenario is marked as requiring attention.
• Message scenarios cannot be saved while any Email step contains a Reply address domain that is not DKIM-enabled.
• New Email steps use `noreply@fs.ocs.oraclecloud.com` as the default Reply address.
• In Fusion Field Service environments, the Reply address is read-only and fixed to the default value.
• In non-Fusion Field Service environments, users can edit the Reply address, but only domains that are DKIM-enabled for the subscription are accepted.
• If DKIM validation cannot be completed during save, the application prevents the configuration from being saved and prompts the user to try again later.
• To use a customer-managed domain as the Reply address domain, users must complete DKIM setup for that domain.

## User Interface Messages

### Configuration page banner

**Action required: Reply address domain isn’t DKIM-enabled.**

One or more message scenarios include email steps with a Reply address from a domain that isn’t DKIM-enabled for this subscription. Emails using that Reply address may not be sent. Update the Reply address in the affected email steps to the recommended noreply@fs.ocs.oraclecloud.com  address or to a DKIM-enabled domain.

Available actions:

• **Review affected scenarios**
• **How-to Register your Domain to Enable DKIM**

**Message scenario list warning**

One or more email steps use a Reply address domain that is not DKIM-enabled.

**Scenario step warning**

Reply address domain is not DKIM-enabled.

**Email step validation error**

Reply address domain is not DKIM-enabled. Choose a Reply address from a DKIM-enabled domain.

**Fusion Field Service read-only message**

Reply address is fixed to the default value and cannot be changed.

**Fusion Field Service save rejection**

Reply address cannot be changed in this environment. It must be noreply@fs.ocs.oraclecloud.com

.

---
*Oracle Cloud Readiness · 26C · SERVICE · Oracle Fusion Field Service*