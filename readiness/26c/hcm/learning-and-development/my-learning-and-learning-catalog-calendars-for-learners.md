[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Learning and Development](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/learning-and-development.md)

# My Learning and learning catalog calendars for learners

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/lear-26c/26C-learning-wn-f49567.htm)

You can now see available instructor-led training and the learning that you're enrolled on your Me > Learning > Calendar page. Use month, week, day, and list views to help you find relevant learning. Drawers with details and in-context actions let you enroll in learning, request enrollment, join waitlists, and view registrations directly from the calendar.

The calendar remembers the last view you used in each browser.

Learner Calendar Showing the Filters Drawer

Learning Catalog Details Drawer

My Learning Details Drawer

Improve learner self-service and engagement by consolidating training discovery and actions in one calendar experience.

## ⚙️ Steps to Enable and Configure

1. Submit the ESS job to create the index definition and perform the initial ingest to OSCS process using this input parameter: fa-hcm-learningrecordtask

Go to Tools > Scheduled Processes.

1. Set the site-level profile value to Yes for the ORA_WLF_ENABLE_SELF_SERVICE_LEARNING_CALENDAR profile option.

## 💡 Tips and Considerations

• By default, the My Learning calendar filter is on, and the Learning Catalog filter is off.
• When both the Learning Catalog and My Learning calendar filters are enabled, only keyword search is available.
• Change the starting day of the week for the calendars in Visual Builder Studio using the SetCalendarDayofWeek page property.

---
*Oracle Cloud Readiness · 26C · HCM · Learning and Development*