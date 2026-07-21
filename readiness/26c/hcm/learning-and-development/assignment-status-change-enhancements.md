[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Learning and Development](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/learning-and-development.md)

# Assignment status change enhancements

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/lear-26c/26C-learning-wn-f49635.htm)

Learning specialists can now manage assignment status changes with more precise control. Some actions were already available in Redwood, and this release adds new restrictions and expands support for specific statuses. This table shows which actions are supported for each learning type and status, what changed, and where restrictions now apply.

Action | Learning Type | Status | Changes
Waitlist | Instructor-led or blended offering | Not Started In Progress Pending Seat Acceptance Pending Fulfilment | Added support for applying this action to these learning types in this Redwood release. It's available now when the learning has capacity enabled.
Event | Pending Seat Acceptance | Added support for this status in this Redwood release. It's available now when the learning has capacity enabled.
Delete | All | Error Deleted Request Rejected Withdrawn Completion Request Rejected | Available in Redwood for specialists with the elevated Delete Learning Assignments privilege.
Undo Complete | All | Incomplete Did Not Attend | Added this action for these statuses in this Redwood release.
Approve | Noncatalog | Completion Request Rejected | Added support for this status in this Redwood release.
Withdraw | Noncatalog | Completion Pending Approval Completion Request Rejected | Removed support for this action and these statuses in this Redwood release.
All | Completed Not Passed Bypass Completed Incomplete Didn't Attend | Added this action for these statuses in this Redwood release. Learning specialists need the Withdraw Completed Assignments privilege to do this action.
Allocate seat | Event Instructor-led or blended offering | Waitlisted | Previously, this action supported only moving the seat to Active status. This Redwood release also supports these options: Grant a Seat, which changes the assignment to Active status Offer a Seat, which changes the assignment to Pending Seat Acceptance status

Improve assignment governance and operational consistency by aligning assignment actions with status-based controls. Support more reliable assignment management across learning operations.

## ⚙️ Steps to Enable and Configure

If you haven't already, enable Redwood Assignment Management to use this feature.

## 🔐 Access Requirements

Learning specialists need these privileges to use assignment actions:

Privilege Name | Code | Description
Withdraw Completed Assignments | WLF_WITHDRAW_COMPLETED_LEARNING_ASSIGNMENTS | Allows withdrawing completed or similar assignments
Delete Learning Assignments | WLF_DELETE_LEARNING_ASSIGNMENTS | Allows deleting assignments

---
*Oracle Cloud Readiness · 26C · HCM · Learning and Development*