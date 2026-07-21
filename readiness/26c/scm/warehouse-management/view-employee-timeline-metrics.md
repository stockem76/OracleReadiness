[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# View Employee Timeline Metrics

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50162.htm)

Warehouse managers need a simple way to review how employees spend time during the day. They need visibility into facility time, work area activity, and break time so they can understand labor usage, identify gaps, and support daily workforce decisions.

With this enhancement, WFM provides a visual employee timeline in the Employee Dashboard. Managers can review an employee’s day in one place instead of relying on the legacy Daily Report.

**INTRODUCING EMPLOYEE TIMELINE METRICS**

WFM now includes a new Employee Timeline Metrics tab in the Employee Dashboard. This tab displays a daily timeline for employees and shows:

• Facility clock-in and clock-out time
• Shift
• Work area activity
• Break time
• Total facility time
• Total work area time
• Total break time
• Open and closed time records

The timeline uses a visual chart so users can quickly see when an employee worked in the facility, moved across work areas, or took breaks. The dashboard includes search filters like Date, Shift, Work Area, and User

The timeline refreshes when users change the company, facility, date, shift, work area, or user filter.

**KEY POINTS TO REMEMBER**:

• Date is required to display timeline data.
• The chart displays data only for the selected day.
• If an employee started work on the previous day and continued into the selected day, that record is not listed for the selected day.
• If an employee started work on the selected day and continued into the next day, that record is listed.
• If an employee has multiple facility clock-in and clock-out records on the same day, WMS shows them separately.
• For open records, WMS uses the current facility time as the end time.
• Work area and break colors come from the existing Work Area and Break setup.

**NOTE:** The legacy Daily Report module and related screens are removed from WFM. Customers should use Employee Timeline Metrics in the Employee Dashboard for daily employee time review.

## ⚙️ Steps to Enable and Configure

1. Open the WFM Employee Dashboard.
2. Select the Employee Timeline Metrics Tab.
3. Enter or select the required date. Optionally, filter by shift, work area, or user.
4. Review the daily timeline for facility time, work area activity, and break time.
5. Review existing Work Area and Break color setup if you want timeline bars to appear with specific colors.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*