[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Maintenance](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/maintenance.md)

# Redwood: Incorporate Ship Method Schedules in Parts Search

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/maint26c/26C-maintenance-wn-f46518.htm)

Capture ship-method schedules and use them when searching for parts.

A new setup UI has been created to capture shipping method pick-up and delivery schedules as shown in the following screen shots. The Parts Search program has been enhanced to use these shipping method schedules in addition to the SCM transit times.

The Parts Search program considers the pick-up time in the source stocking location time zone and the delivery time in the ship-to address time zone. It doesn't use the distance limitation, which is planned for a future release. It also continues to use SCM transit times to identify stocking locations with the required part(s), but lead times are now derived from the new Shipping Method Schedule UI rather than the Transit Times UI.

Shipping Method Schedules

Create Shipping Method Schedule

The Parts Search UI has been enhanced to display the ship-to address along with the expected ship and arrival dates/times.

Part Search UI

While incorporating shipping method schedules into our Parts Search logic, we have also enhanced the way it calculates expected ship and arrival dates/times as described below:

**Earliest Ship and Arrival**

1. When a need-by date is NOT entered on the part requirement, the Parts Search program uses Shipping Method Schedules to determine the **earliest** each ship method can deliver the parts to the ship-to address.
2. Expected Ship Date/Time is the pick-up time on next day that the ship method is available.
3. Expected Arrival Date is the expected ship date plus the shipping method lead time days.
4. Expected Arrival Time is the shipping method delivery time.

**Latest Ship Date and Arrival**

1. When a need-by date is entered on the part requirement or Parts Search UI, the Parts Search program uses Shipping Method Schedules to look for the latest date/time the parts can be shipped and still meet the need-by date/time.
2. Expected Ship Date/Time is the pick-up time on last date the shipping method can meet the need-by date and time.
3. Expected Arrival Date is the expected ship date plus the shipping method lead time.
4. Expected Arrival Time is the shipping method delivery time.

The parts search now calculates more accurate ship and arrival dates/times providing better customer service and coordination with the arrival of the field service technician.

## ⚙️ Steps to Enable and Configure

Shipping method schedules must be set up to use this new feature as described.  If shipping method schedules aren't set up, there is no change to the parts search logic. (Retains current functionality).

## 🔐 Access Requirements

Users who are assigned a configured job role that contains these privileges can access this feature:

• Access Standalone Parts Ordering Page (RCL_PARTS_ACCESS_STANDALONE_PAGE)
• View Requirement Lines (RCL_PARTS_REQ_VIEW)

---
*Oracle Cloud Readiness · 26C · SCM · Maintenance*