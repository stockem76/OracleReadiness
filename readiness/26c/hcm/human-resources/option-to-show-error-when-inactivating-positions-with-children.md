[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Human Resources](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/human-resources.md)

# Option to Show Error when Inactivating Positions with Children

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hure-26c/26C-hr-wn-f44426.htm)

We have introduced a new profile option that enables you to show an error message when a user tries to inactivate a position having one or more active child positions currently or in the future.

Earlier, a warning was shown in this scenario. The user had the option to ignore the warning and inactivate the position without reassigning the child positions to a different parent position. If they inactivated the position in spite of the warning, the associated records could be impacted.

With this new error message, the user can’t inactivate the position until they reassign the child positions to a different parent position.

The error message ensures that a user can’t inactivate a position that has child positions until they first reassign the child positions to a different parent position. This prevents any associated records from being impacted.

## ⚙️ Steps to Enable and Configure

To show an error instead of a warning, you need to set the value of the ORA_PER_INACTIVATE_POS_W_CHILD profile option to **Error**. The default value is **Warning**. For more information about how you set the value of a profile option, see How do I enable a profile option?

---
*Oracle Cloud Readiness · 26C · HCM · Human Resources*