[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# Redwood: Use Time Zone in Cycle Count Sequences

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f46480.htm)

For global organizations operating across multiple time zones, accurate and timely inventory management is critical to daily operations. When some organizations operate in regions far ahead of coordinated universal time (UTC), they can face challenges if their time zone isn't considered during scheduling. Prior to this update, cycle counts schedules were created without a time zone reference, which sometimes caused dates to fall on the previous day. Now, cycle counts consider a user’s local time zone preferences when creating cycle counts and generating schedules.

This feature now enables time zone-aware cycle count processing so that cycle count dates are defaulted, evaluated, and generated based on the organization’s time zone instead of UTC. This ensures that cycle count schedules and sequences are created on the intended local business day and not shifted due to UTC-based processing.

This table provides examples of how cycle count dates behave with time zone enabled and disabled scenarios, including existing data and cross time zone access.

Scenario | Org Time Zone | Cycle Count Record Stamp | Start Date (UI) | Count Sequence Date
New Record (Opt-In Enabled) | Sydney (UTC+10) | 28-01-2026  08:00:00 | 28-01-2026 | 28-01-2026
New Record (Opt-In Disabled) | Sydney (UTC+10) | 28-01-2026  08:00:00 | 27-01-2026 | 27-01-2026
Existing Record (Opt-In Enabled) | New York (UTC-5) | 26-03-2025 | 25-03-2025 | Follows organization's time zone after conversion
Existing Record (Opt-In Disabled) | New York (UTC-5) | 26-03-2025 | 26-03-2025 | Follows UTC-based evaluation (no conversion)

This feature ensures that cycle counts are generated with the correct business date, allowing organizations to operate seamlessly across geographies while maintaining accurate records and improving process efficiency.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Manufacturing and Supply Chain Materials Management*

## 💡 Tips and Considerations

• When enabled, cycle count dates are determined and displayed based on the organization’s time zone, ensuring alignment with the local business day.
• Dates are displayed as date-only values (no time component), even though time zone conversion is applied in the background.
• For existing cycle count data (without a time component), the stored date is assumed to be UTC midnight. When converted to the organization's time zone, this may result in the displayed date shifting to the previous local day.
• The user-preferred time zone doesn't impact the date display or evaluation. All users within the same organization see consistent dates based on the organization's time zone.
• For organizations where the time zone isn't configured (null), enabling the opt-in doesn't change existing behavior. Cycle count processing continues to follow UTC.

## 🔐 Access Requirements

No additional access is required.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: Using Inventory Management guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*