[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Revenue Contract Realignment

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f50398.htm)

Reassign performance obligations between revenue contracts to correct any misidentified contract arrangements, ensuring that obligations originating from multiple orders are accurately consolidated into a single contract. This supports compliance with ASC 606 and IFRS 15, improves revenue accuracy, and preserves data integrity across all orders and contracts.

Revenue managers use the Edit Customer Contract page to select performance obligations from the source contract. The user then selects the Reassign Performance Obligations action from the Performance Obligations tab to select the target contract and reassignment details to submit the reassignment. Submitting the reassignment triggers the Identify Customer Contracts process to move the selected performance obligations to the target contract. The target contract must use the same ledger and currency as the source contract. When a performance obligation contains multiple promised detail lines, all lines in that performance obligation are moved together.

Once the reassignment is completed, the selected performance obligations are transferred to the target contract. Both the source and target contracts are reallocated as material revisions.  Users can view the reassignment history by selecting View Performance Obligations Reassignment Details from the contract header actions menu in either source or target contract

**Key Capabilities:**

• Reassign performance obligations from an existing source contract to an existing target contract.
• Select the Reassign Performance Obligations action from the Performance Obligations tab.
• Capture target contract, accounting treatment, reason, and comments during reassignment.
• Submit the reassignment which triggers the Identify Customer Contracts process.
• Track reassignment history, including source and target performance obligation numbers, contract numbers, status, request number, submission date, and submitted by details.
• Show the source contract status as Reassigned when no performance obligations remain after reassignment.

**Business Benefits include:**

• Allows revenue teams to correct contract grouping issues without manual workarounds.
• Improves revenue accuracy.
• Helps preserve contract and obligation history.
• Supports compliance with revenue recognition requirements such as ASC 606 and IFRS 15.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• Source and target contracts must have the same ledger and currency.
• Reassignment is supported only to an existing revenue contract.
• Performance obligations are reassigned as new performance obligations in the target contract.
• Both the source and target contracts are reallocated as material revisions.
• If the target contract is discarded after reassignment, the discard process may create two new contracts, and the reassignment may need to be performed again.

## 🔐 Access Requirements

No new access requirements.

---
*Oracle Cloud Readiness · 26C · ERP · Financials*