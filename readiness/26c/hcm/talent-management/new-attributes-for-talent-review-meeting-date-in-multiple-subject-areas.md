[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# New Attributes for Talent Review Meeting Date in Multiple Subject Areas

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f49895.htm)

You can now capture and track precise meeting and submission timelines in Talent Review with the introduction of timestamp-based Meeting Date and Deadline Date attributes. These attributes help provide greater accuracy and visibility into talent review scheduling and submission activities for improved planning, tracking, and reporting.

As a HR Administrator, you can report on the accurate data submission deadline date along with the timestamp to accurately understand the true submission deadline for managers.

  Also, you can report on the accurate meeting date along with the timestamp to accurately understand the true meeting date for participants of the meeting

## ⚙️ Steps to Enable and Configure

Use the newly added attributes for your reporting requirements.

Subject Area | Folder | Attribute
Workforce Talent Review -  Talent Review Meeting Real Time | Talent Review Meeting Details | Deadline for Submitting Ratings with Time
 |  | Meeting Date and Time
Workforce Talent Review -  Talent Review Tasks Real Time | Talent Review Meeting Details | Deadline for Submitting Ratings with Time
 |  | Meeting Date and Time
Workforce Profiles - Feedback Notes by Recipient Real Time | Meeting Details | Deadline for Submitting Ratings with Time
 |  | Meeting Date and Time

## 💡 Tips and Considerations

Existing Meeting Date attribute and new attribute Meeting Date and Time may render different dates based on the time zone the user has preferred in the system.

For example, if a Talent Review Meeting is scheduled for 26/May/2026 9:00 AM AEST (Sydney Australia)

  Meeting Date attribute will render 25/May/2026 (Date is saved post converting to UTC (Coordinated Universal Time) zone)

  Meeting Date and Time attribute will render 26/May/2026 9:00 AM (Date is saved post converting to UTC (Coordinated Universal Time) zone, however OTBI renders the date converted to the user preferred time zone.)

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*