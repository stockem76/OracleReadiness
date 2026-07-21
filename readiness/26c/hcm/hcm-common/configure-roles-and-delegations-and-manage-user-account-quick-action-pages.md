[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [HCM Common](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/hcm-common.md)

# Configure Roles and Delegations and Manage User Account Quick Action Pages

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hcom26c/26C-hcm-common-wn-f49533.htm)

You can now use business rules to control the display of page elements on the **Roles and Delegations** and **Manage User Account** quick action pages.

This feature helps administrators simplify the user account management experience by controlling the visibility of page elements and displaying only the information that is most relevant to their business processes.

You can control visibility of the following sections:

• Roles
• Role Delegations
• Approval Delegation Rules
• Roles Delegated to Me

You can control visibility of the following fields:

• Roles 
  • StartDate
• Role Delegations 
  • EndDate
• Approval Delegation Rules 
  • EndDate
• IsSelfApprovalEnabled

You can control visibility of the following actions:

• User 
  • HideEditAction
• Roles 
  • HideAddRoles
• HideDeleteRoles
• Role Delegations 
  • HideAddRoleDelegation
• HideEditRoleDelegation
• Approval Delegation Rules 
  • HideAddAction
• HideEditAction
• Roles Delegated To Me 
  • HideDeleteAction
• PageLevelActions 
  • HideCreateUserAccount
• HideLinkUserAccount
• HideProcessUserAccountStatus
• HideResetPassword
• HideSyncWithIdentityStore
• HideUpdateRolesAssignments

You can also configure the following elements to be optional or required:

• Role Delegations 
  • EndDate
• Approval Delegation Rules 
  • EndDate

This feature provides the flexibility to configure the Account Management page without requiring custom code. These configurations help tailor the user experience to align with user roles and organizational requirement

## ⚙️ Steps to Enable and Configure

Leverage the Visual Builder Studio to expose your applications. To learn more about extending your application using Visual Builder, visit Oracle Help Center > *your apps service area of interest* > Books > Configuration and Extension.

No additional enablement is required beyond configuring field visibility through business rules in Visual Builder Studio.

## 🔐 Access Requirements

There are no extra access requirements for this feature.

---
*Oracle Cloud Readiness · 26C · HCM · HCM Common*