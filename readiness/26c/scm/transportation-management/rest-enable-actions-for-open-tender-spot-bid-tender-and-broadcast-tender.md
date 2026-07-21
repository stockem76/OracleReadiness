[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# REST Enable Actions for Open Tender - Spot Bid Tender and Broadcast Tender

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f49509.htm)

This feature supports Open Tender via REST services, allowing you can integrate Open Tender activities into AI Agents and other external transportation management processes.

The REST enabled Shipment Business Actions include the following REST APIs:

• getOpenTenderServiceProviderOptions
• Added to support the UI actions 'Spot Bid Tender' and 'Broadcast Tender' by retrieving service provider options for shipments. This API returns feasible and infeasible service provider options.
• getOpenTenderServiceProviderOptions
• custom-actions/getOpenTenderServiceProviderOptions/shipments
• custom-actions/getOpenTenderServiceProviderOptions/shipments/{shipmentId}
• submitOpenTender
• Added to support the UI actions 'Spot Bid Tender' and 'Broadcast Tender' for shipments. This API submits open tender offers to the selected service providers for one or more shipments.
• submitOpenTender
• custom-actions/submitOpenTender/shipments
• custom-actions/submitOpenTender/shipments/{shipmentId}
• withdrawOpenTender
• Added to support the UI actions 'Withdraw Spot Bid Tender' and 'Withdraw Broadcasted Tender' for shipments. This API withdraws previously submitted open tender offers for one or more shipments.
• withdrawOpenTender
• custom-actions/withdrawOpenTender/shipments
• custom-actions/withdrawOpenTender/shipments/{shipmentId}

• Get open tender service provider options for a shipment
• Get open tender service provider options for one or more shipments
• Submit open tender offers for a shipment
• Submit open tender offers for one or more shipments
• Withdraw open tender offers for a shipment
• Withdraw open tender offers for one or more shipments

**Business Benefit:**This feature extends the options available to you for automating your Open Tender workflows using AI Agents.  The provided REST enabled business actions will allow you to develop AI Agents that can review available service providers for your open tender, initiate the open tender and, if necessary, withdraw the open tender

## ⚙️ Steps to Enable and Configure

1. Verify that your integration users have access to the applicable REST API services and shipment data.
2. Identify the shipment or shipment groups that will participate in an open tender - Spot Bid Tender or Broadcast Tender workflows.
3. Use the appropriate REST API endpoint based on your business process: 
  • Retrieve service provider options: 
    • custom-actions/getOpenTenderServiceProviderOptions/shipments
• custom-actions/getOpenTenderServiceProviderOptions/shipments/{shipmentId}
• Submit open tenders: 
    • custom-actions/submitOpenTender/shipments
• custom-actions/submitOpenTender/shipments/{shipmentId}
• Withdraw open tenders: 
    • custom-actions/withdrawOpenTender/shipments
• custom-actions/withdrawOpenTender/shipments/{shipmentId}
4. For bulk operations, provide the required shipment information in the request payload.
5. Review the returned service provider options before submitting tenders to ensure the selected providers align with your operational requirements.
6. Use the withdrawal API when shipment conditions change or when open tenders should no longer remain active.

No additional user interface configuration is required if you already use Spot Bid Tender or Broadcast Tender workflows.

## 💡 Tips and Considerations

• The Get open tender service provider options API returns both feasible and infeasible providers. Review the response carefully before submitting tenders.
• Bulk endpoints can help improve efficiency when processing multiple shipments in a single operation.
• Withdrawal actions only apply to previously submitted open tenders.
• Single-shipment endpoints may support optional request payloads, while bulk endpoints require request body details.
• Ensure that external integrations properly handle response validation and error handling when processing tender submissions or withdrawals.
• Use these APIs in conjunction with existing shipment lifecycle and tender management processes to maintain operational consistency.
• If your organization uses automated tendering workflows, validate service provider eligibility rules before integrating large-scale automation processes.

## 📚 Key Resources

For more complete documentation and information see: https://docs.oracle.com/en/cloud/saas/transportation/26c/otmra/index.html

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*