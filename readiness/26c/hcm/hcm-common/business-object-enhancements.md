[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [HCM Common](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/hcm-common.md)

# Business Object Enhancements

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hcom26c/26C-hcm-common-wn-f46315.htm)

**BUSINESS OBJECTS WITH NEW COMPONENTS**

The following business object has introduced a new component in the hierarchy.

*Payroll Localization - United States*

**Tax Withholding (TaxWithholding.dat)**

Component | Description
State Taxes IA 2026 (StateTaxesIA2026) | Fields that are effective from 1st January 2026 for State Taxes IA.

.

**BUSINESS OBJECTS WITH NEW ATTRIBUTES**

*Absence Management*

**Absence Accrual Balance Component (PersonAccrualDetail.dat)**

Component | New Attributes
Absence Accrual Balance Component (PersonAccrualDetail) | DisbursementReason

.

*Compensation*

**Market Data Survey Data (MktSurveyData.dat)**

Component | New Attributes
Market Data Survey Data (MktSurveyData) | BatchEndDate (Batch End Date) BatchStartDate (Batch Start Date)

.

*Global HR - Work Structures*

**Location (Location.dat)**

Component | New Attributes
Location (Location) | DeliverToSiteFlag (Deliver-to Site) ReceivableMaterials (Receivable Materials)

.

*Health and Safety*

**Incident Summary (IncidentSummary.dat)**

Component | New Attributes
Incident Event (IncidentEvent) | EventErgonomicAssReqCode

.

*Learning*

**Learning Record Activity Attempt V3 (LearningRecordActivityAttemptV3.dat)**

Component | New Attributes
Learning Record Activity Attempt V3 (LearningRecordActivityAttemptV3) | TaskOwner (Task Owner)

.

*Global Payroll - Balances*

**Balance Adjustment Line (BalanceAdjustmentLine)**

Component | New Attributes
Balance Adjustment Line (BalanceAdjustmentLine) | PayrollComponentId PayrollComponentCode

.

**Balance Initialization Batch Line (InitializeBalanceBatchLine.dat)**

Component | New Attributes
Balance Initialization Batch Line (InitializeBalanceBatchLine) | PayrollComponentId PayrollComponentCode

.

*Talent Management*

**Talent Review Meeting (TalentReviewMeeting.dat)**

Component | New Attributes
Talent Review Meeting (TalentReviewMeeting) | MeetingTimestamp (Meeting Date and Time) DataSubmitTimestamp (Ratings Submission Date and Time)

Use the **View Business Objects**task to review and download the latest business object information.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 📚 Key Resources

Additional guidelines and examples are available in the HCM Data Loader Business Objects guide.

---
*Oracle Cloud Readiness · 26C · HCM · HCM Common*