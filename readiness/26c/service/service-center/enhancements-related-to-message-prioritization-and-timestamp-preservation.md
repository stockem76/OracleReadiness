[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Service Center](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/service-center.md)

# Enhancements Related to Message Prioritization and Timestamp Preservation

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/bsvc-26c/26C-b2b-service-wn-f47320.htm)

Fusion Service now includes enhancements that help agents highlight urgent Service Request communications and support timestamp preservation during data migration.

Agents can mark replies as high priority to clearly indicate communications that require prompt attention. This helps recipients quickly recognize time-sensitive messages and take action sooner.

Fusion Service also supports optionally setting MessageLastUpdateDate through the payload. This capability is controlled by the SVC_ALLOW_UPDATE_TO_MESSAGE_LAST_UPD_DATE profile option and is intended for migration and integration scenarios where original message timestamps need to be preserved.

By default, existing behavior remains unchanged. Unless the profile option is explicitly enabled, Fusion Service continues to derive MessageLastUpdateDate from LastUpdateDate

.

• Helps agents clearly signal urgent customer communications.
• Improves visibility for messages that require timely customer action.
• Supports more accurate timestamp preservation during data migration.
• Maintains backward compatibility by keeping existing behavior as the default.
• Provides controlled opt-in behavior for customers who need migration-specific timestamp handling

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• High-priority marking is intended for replies where customer attention or action is time-sensitive.
• Timestamp preservation is primarily intended for migration and integration use cases.
• Existing customers are not impacted unless the timestamp-preservation option is explicitly enabled.

---
*Oracle Cloud Readiness · 26C · SERVICE · Service Center*