[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# GLOBAL UPTAKE: RETROACTIVE OVERPAYMENT AND RECOVERY FOR TIMECARD AND ABSENCE ELEMENTS

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f50107.htm)

The Retroactive Overpayment and Recoveries feature has been extended to support US Timecard and Absence elements. This feature was first introduced in Update 25D for Standard Earnings elements and later extended to include Supplemental Earnings elements.

With this enhancement, you can process retroactive timecard or absence overpayments through the **Recoveries** calculation card and recovered over multiple pay periods rather than in a single period, reducing the impact on the employee’s net pay.

A new element template question, **Is this element subject to retroactive recoveries**, is now available when creating timecard or absence elements.

The options for the template question are:

• Yes
• No

The question is set to **No** by default. Setting the question to **Yes** creates the elements required to generate the Recoveries card.

For info on the Overpayment Recovery report, see How do I use the Overpayment Recovery report to manage retroactive recoveries that I have identified? in the Help Center.

This enhancement helps customers manage retroactive timecard and absence overpayments more effectively by automatically creating recovery entries for eligible cases and allowing repayments to be spread across multiple pay periods. This reduces the impact on employee net pay, improves recovery tracking, and provides better visibility into outstanding retroactive overpayments through delivered reporting.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• This feature applies to new timecard or absence elements. It doesn’t impact elements you’ve already defined.
• Absence elements configured to **Reduce regular earnings by absence payment** don’t create recovery cards when retroactive adjustments:
1. Offset each other.
2. Result in no recoverable overpayment.

Recovery cards are created only when the retroactive result reflects a true negative overpayment.

• Absence elements set up with payment and deduction rate definitions use a different processing path. Depending on the retroactive results generated, recovery cards may be created even when the retroactive adjustments offset each other.

## 📚 Key Resources

How do I use the Overpayment Recovery report to manage retroactive recoveries that I have identified?

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*