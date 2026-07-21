[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Additional Attributes Inclusion in Fast Formula

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f49465.htm)

From this release you can include the goal plan ID and the descriptive flexfields (DFFs) of a goal plan in fast formulas such as fast formulas used to calculate the eligibility for goal assignment. You create fast formulas using the **Manage Fast Formulas** task in the Setup and Maintenance work area. To the fast formula you can now add these database items (DBI):

• **Goal Plan ID**: HRG_GOAL_PLANS_GOAL_PLAN_ID
• **DFFs:** HRG_GOAL_PLANS_ATTRIBUTEn

Here’s an example fast formula that checks the department name of a person and uses the goal plan ID to retrieve the goal plan name. It creates an eligibility profile to assign the 'Goal Plan_Q2_2026’ goal plan to employees of the ‘Marketing’ department.

/* DATABASE ITEM DEFAULTS BEGIN */
DEFAULT FOR ELIGIBLE IS 'N'

DEFAULT_DATA_VALUE FOR HRG_GOAL_MASS_REQUESTS_PARENT_ID IS 0

DEFAULT_DATA_VALUE FOR HRG_GOAL_MASS_REQUESTS_GOAL_PLAN_ID IS 0

DEFAULT_DATA_VALUE FOR HRG_GOAL_MASS_REQUESTS_MASS_REQUEST_ID is 0

DEFAULT_DATA_VALUE FOR HRG_GOAL_PLANS_GOAL_PLAN_ID IS 0
DEFAULT_DATA_VALUE FOR HRG_GOAL_PLANS_GOAL_PLAN_NAME IS 'NA'
DEFAULT FOR PER_ASG_ORG_DEPARTMENT_NAME IS ' '
DEFAULT FOR PER_ASG_PERSON_ID IS 0
/* DATABASE ITEM DEFAULTS END */
INPUTS ARE IV_ELIG_OBJ_COLUMN_NAME (text)
l_col = IV_ELIG_OBJ_COLUMN_NAME
J=1
l_goal_plan_id=-1
l_parent_id=-1
l_goal_plan_name='NA'
l_department_name ='NA'
l_child_mass_req_id=-1
ELIGIBLE='N'
while (HRG_GOAL_MASS_REQUESTS_MASS_REQUEST_ID.exists(J))
loop
(
IF (HRG_GOAL_MASS_REQUESTS_MASS_REQUEST_ID[J] = TO_NUMBER(l_col))
  THEN
   ( l_parent_id=HRG_GOAL_MASS_REQUESTS_PARENT_ID[J]
 EXIT)
   J=J+1
)
I=1
while (HRG_GOAL_MASS_REQUESTS_MASS_REQUEST_ID.exists(I))
loop
(
IF (HRG_GOAL_MASS_REQUESTS_MASS_REQUEST_ID[I] = l_parent_id)
  THEN
   IF (HRG_GOAL_MASS_REQUESTS_MASS_REQUEST_ID[I] = l_parent_id)
  THEN
    (l_goal_plan_id=HRG_GOAL_MASS_REQUESTS_GOAL_PLAN_ID[I]

 EXIT)
 
    I=I+1
)
K=1
while (HRG_GOAL_PLANS_GOAL_PLAN_ID.exists(K))
loop
(
IF (HRG_GOAL_PLANS_GOAL_PLAN_ID[K] = l_goal_plan_id)
  THEN
    (l_goal_plan_name=HRG_GOAL_PLANS_GOAL_PLAN_NAME[K]
     EXIT)
    K=K+1
)
l_department_name = PER_ASG_ORG_DEPARTMENT_NAME
RET=ESS_LOG_WRITE('l_department_name ='||l_department_name)
IF (l_goal_plan_name='Goal Plan_Q2_2026') AND (l_department_name like ' Marketing%')
THEN (ELIGIBLE='Y')
return ELIGIBLE

## 🎯 Business Benefit

Control goal plan assignment using fast formulas and enhance goal management in your organization.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 📚 Key Resources

For more information on managing fast formulas, see the Administering Fast Formulas guide on Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*