[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Split Installments Based on Payment Threshold Amount for Japan Supplier Payments

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49476.htm)

Oracle Payables now supports splitting supplier payment installments based on configurable payment threshold amounts to address common payment practices in Japan. Organizations can automatically divide supplier payments into immediate and deferred portions when the total payment amount exceeds a defined threshold.

This feature enables companies to improve cash flow management by paying a percentage of the invoice amount immediately through bank transfer while deferring the remaining balance using bills payable or cash on due (COD) payment methods.

You can define split payment rules at the supplier payment method assignment level.

During the payment process request (PPR) flow, Oracle Payables evaluates the calculated payment amount and automatically performs the following actions:

• Splits installments when the payment threshold is exceeded
• Updates payment methods based on the configured split rules
• Creates new installments when required
• Defers selected installments by updating the payment method for bills payables payments
• Defers selected installments by updating due dates and payment method for COD payments
• Removes deferred installments from the current payment run
• Continues processing installments associated with the immediate payment method within the same PPR

The feature supports:

• Supplier payments in JPY as well as all other currencies
• Bills payable and COD payment scenarios
• Credit and debit memos
• Prepayment invoices
• Withholding tax recalculation
• Discount handling
• Interest invoice handling

This feature helps organizations operating in Japan:

• Improve cash flow management by deferring a portion of supplier payments
• Automate installment splitting based on configurable business rules
• Support common Japanese payment practices such as bills payable and cash on due
• Ensure consistent application of payment splitting policies
• Support compliance with regional business payment practices
• Maintain flexibility through configurable split percentages, thresholds, and payment methods

1. Enable the feature through development opt-in.
2. Designate specific payment methods as split payment methods and assign them as the primary payment methods for suppliers to whom installment splitting applies.
3. In the selected split payment method, enable the Payment Split Rule option to define split payment rules at the supplier payment method assignment level. .
4. Configure the splitting rules using the following attributes based on the agreed terms with each supplier:
• Payment threshold amount – 
• Enter the payment amount threshold above which the installments will be split.
• Payment currency – 
• Enter the payment currency code for which the split should be applied.
• Deferred payment method (Bills payable or COD payment method)
• This should not be equal to the payment method against which the split rules are defined.
• Enter either bills payable or non-bills payable payment method. If a non-bills payable payment method is entered, it is treated as Cash on due payment.
• If non-bills payable payment method is entered, provide a value for the 'Due date increment days'.
• Deferred payment percentage (bills payable or cash on due payment percentage) – 
• Enter the percentage of the payment amount to be deferred. The maximum allowed value is 100.
• If the value entered is 100, the entire payment amount will be deferred.
• Due date increment days (for COD) -
• If non-bills payable payment method is selected for deferred payment method, value should be provided in the ‘due date increment days’.
• This value is used to increase the installment due date.
• Immediate payment method -
• Enter the payment method to be used for the immediate payment (bank transfer). This method must be different from both the split payment method and the deferred payment method (bills payable/cash on due payment method).
• Immediate payment percentage -
• This is a read-only field.
• This value is calculated automatically and displayed when the deferred payment percentage (bills payable or cash on due payment percentage) is entered.
• The value is calculated by subtracting the deferred percentage from 100.
• Round Down –
• Optionally, deferred payment amount can be rounded to nearest Ones, tens or hundreds or thousands value.
5. Create the invoices.
6. Submit payment process requests (PPRs).
7. After selecting the invoices, application splits the installments automatically if the payment amount exceeds the threshold limit based on the splitting rules for each of the suppliers

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Financials*

## 💡 Tips and Considerations

Key tips and considerations include:

• The feature is intended specifically for Japan payment processing requirements.
• The maximum number of splits supported is two.
• Split rules can be defined at supplier site, address, and profile levels.
• Deferred installments updated with bills payable or COD payment methods are removed from the current payment process request.
• Interest invoices are excluded from split amount calculations.
• Prepayment invoice, debit memos and credit memos are supported during the split.
• If a split rule is inactive during payment processing, the affected installments are removed from payment processing.
• During installment splitting, the PPR will be in a new status: **‘Waiting for Installment Split’**.
• The installment split process is irreversible. During the PPR run, once the installment split process is completed, terminating the PPR will not reverse the split, and the installments will retain the post-split amounts
• Split installments based on the payment threshold amount are not supported for quick payments, manual payments, and pay-in-full payments.
• Split installments are supported for supplier payments only. One time payment requests, Customer refunds, employee reimbursements are out of scope.
• Split processing is supported only for EFT payments. Check payments and virtual card payments are not supported.
• Support for defining splitting rules through FBDI import is not supported.

## 🔐 Access Requirements

Users must have the required Payables and Payments setup privileges to:

• Configure supplier payment methods
• Define split payment rules
• Submit payment process requests
• Review payment processing reports
• Manage supplier payment configurations

## 📚 Key Resources

Related Help:

• Manage Supplier Payment Methods in the Oracle Fusion Cloud Financials Implementing Payables and Payments guide
• Manage Payment Process Requests in the Oracle Fusion Cloud Financials Using Payables guide

---
*Oracle Cloud Readiness · 26C · ERP · Financials*