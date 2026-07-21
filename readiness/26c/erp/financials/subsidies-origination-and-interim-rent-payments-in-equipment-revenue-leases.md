[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Subsidies, Origination, and Interim Rent Payments in Equipment Revenue Leases

`🔧 Optional Uptake` · `⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49382.htm)

Create and bill one-time payments for subsidy, origination charges, and interim rent at lease inception, associating each payment with specific assets. Automatically generate revenue recognition schedules and accounting entries for these payments.

To create leases with payments for interim rent, subsidies, and origination charges:

1. Create an equipment revenue lease and add assets.
2. Create rent payments by selecting Payment Category as Rent and Payment Phase as Base Term. 
  • Select a payment template and associate each payment to an asset.
• The payment and transaction tax details default from the payment template and may be updated as needed.
• Update the payment details such as payment amounts, frequency, and number of payments.
3. Create one-time payments for interim rent payment by selecting Payment Category as Rent and Payment Phase as Interim. 
  • Select a payment template and associate each payment to an asset.
• The payment and transaction tax details default from the payment template and may be updated as needed.
• Update the payment amount.
4. Create one-time payments for subsidy by selecting Payment Category as Subsidy. 
  • Select a payment template and associate each payment to an asset.
• The payment and transaction tax details, accrual type, and accounting distributions default from the payment template and may be updated as needed.
• Update the payment amount.
5. Create one-time payments for origination charges by selecting Payment Category as Origination. 
  • Select a payment template and associate each payment to an asset.
• The payment and transaction tax details, accrual type, and accounting distributions default from the payment template and may be updated as needed.
• Update the payment amount.
6. Validate the lease and generate schedules.
7. Review the payment and income amortization schedules for rent, interim rent, subsidies, and origination charges before activating the lease: 
  • For operating leases, the total revenue from rent and interim rent is evenly spread over the revenue recognition term as rental accrual.
• Income amortization schedules are generated for subsidies and origination charges when the Accrual Type is Upfront or Amortized.
8. Approve and activate the lease.

The following screenshots describe creating payments and viewing schedules for rent, interim rent, subsidies, and origination charges:

Create Payment page - Interim Rent

Create Payment page - Subsidy

Payment Details Accounting tab - Subsidy

Create Payment page - Origination

Payment Details Accounting tab - Origination

Schedules - Amortization Summary

Business benefits include:

• Improves billing accuracy and efficiency by automating early-stage lease payment processes.
• Ensures timely revenue recognition and compliance with accounting standards for subsidy, and origination payments.

## ⚙️ Steps to Enable and Configure

Use the Opt In UI to enable this feature. For instructions, refer to the Optional Uptake of New Features section of this document.

Offering: *Financials*  No Longer Optional From: *Update 27A*

If you plan to adopt this feature, then you must log an SR with Oracle Support to get a code.

Perform the following setups:

Create Accounting Template:

1. Navigate to Search Accounting Templates under Manage Lease Accounting Configuration.
2. Create Accounting Template and enter Business Unit, Accounting Template Name and Description.
3. Select the primary and secondary accounting classifications and distributions for accounting the rental accrual, rent and interim rent payments for the leased asset.
4. Update the accounting template status to Active.

Update Accounting Template page

Create Payment Template for rent payments:

1. Navigate to Search Revenue Lease Payment Templates under Manage Lease Accounting Configuration.
2. Create Payment Template and enter Business Unit and Payment Template Name.
3. Select the Asset Type as Equipment, Payment Category as Rent, and Payment Phase as Base Term.
4. Enter payment and transaction tax details.
5. Update the payment template status to Active.

Update Revenue Lease Payment Template page - Rent

Create Payment Template for interim rent payments:

1. Navigate to Search Revenue Lease Payment Templates under Manage Lease Accounting Configuration.
2. Create Payment Template and enter Business Unit and Payment Template Name.
3. Select the Asset Type as Equipment, Payment Category as Rent, and Payment Phase as Interim.
4. Enter payment and transaction tax details.
5. Update the payment template status to Active.

Update Revenue Lease Payment Template page - Interim Rent

Create Payment Template for subsidies:

1. Navigate to Search Revenue Lease Payment Templates under Manage Lease Accounting Configuration.
2. Create Payment Template and enter Business Unit and Payment Template Name.
3. Select the Asset Type as Equipment and Payment Category as Subsidy.
4. Enter payment and transaction tax details, and distributions for accounting the subsidy.
5. Select the Accrual Type: 
  • Amortize – Spread the subsidy income over the asset term in proportion to the lease revenue accrual.
• Upfront – Recognize the subsidy income upfront in the first period of the asset term.
• None - Do not generate income amortization.
6. Update the payment template status to Active.

Update Revenue Lease Payment Template page - Subsidy

Create Payment Template for origination charges:

1. Navigate to Search Revenue Lease Payment Templates under Manage Lease Accounting Configuration.
2. Create Payment Template and enter Business Unit and Payment Template Name.
3. Select the Asset Type as Equipment and Payment Category as Origination.
4. Enter payment and transaction tax details, and distributions for accounting the origination charge.
5. Select the Accrual Type: 
  • Amortize – Spread the origination income over the asset term in proportion to the lease revenue accrual.
• Upfront – Recognize the origination income upfront in the first period of the asset term.
• None - Do not generate income amortization.
6. Update the payment template status to Active.

Update Revenue Lease Payment Template page - Origination

## 🔐 Access Requirements

No new access requirements.

## 📚 Key Resources

Based on Idea 639735 from the Lease Accounting Idea Lab on Oracle Cloud Customer Connect.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*