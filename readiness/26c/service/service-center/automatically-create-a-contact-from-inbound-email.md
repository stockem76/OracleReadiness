[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Service Center](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/service-center.md)

# Automatically create a Contact from inbound email

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/bsvc-26c/26C-b2b-service-wn-f47288.htm)

This feature provides profile options that your administrator can enable to automatically create new Contacts from inbound emails, if the Contact details are not already found in the database by the email processing system. This feature also allows your implementation to define a default first name and last name for each new contact if the email address is void of a discernable first name and last name.

The profile options are

• **ORA_SVC_INBOUND_MSG_AUTO_CONTACT_CREATION_ENABLED** - When enabled, a new Contact is created with the details from the inbound email, if matching Contact details are not found in the Fusion Service database.
• **ORA_SVC_CONTACT_DEFAULT_FIRST_NAME** - Allows the administrator to provide a default first name for the Contact, if the inbound email address lacks first name. The default value is 'Default First Name'.
• **ORA_SVC_CONTACT_DEFAULT_LAST_NAME** - Allows administrator to provide a default last name for the Contact, if the inbound email address lacks last name. The default value is 'Default Last Name'.

In previous releases, if a new SR was created from an inbound email from an unknown contact, the SR would be created but the Primary Contact field would be left empty. WIth this new option, the email processing process will automatically create a new contact when required and associate it as the primary contact of the SR.

The simplifies SR handling because a user does not need to manually create a new contact record and associate it to the SR. The enhancement also makes SR handling more consistent because Primary Contact field will always be populated.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

The profile option SVC_ENABLE_INBOUND_EMAIL_DEFAULT_PROCESSING used for creating Service Requests from emails should be enabled first and then the new profile option to create Contacts should be enabled.

---
*Oracle Cloud Readiness · 26C · SERVICE · Service Center*