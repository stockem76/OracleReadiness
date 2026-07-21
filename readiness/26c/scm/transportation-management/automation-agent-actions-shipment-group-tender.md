[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# Automation Agent Actions - Shipment Group Tender

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f49507.htm)

This feature provides you with the following Shipment Group tender agent actions, providing you with the option of fully automating the entire Shipment Group tender use case.

Shipment Group Tender Agent Actions:

• TENDER SHIP GROUP
• ACCEPT SHIPMENT GROUP TENDER
• WITHDRAW SHIPMENT GROUP TENDER with Decline Reason Code

**Business Benefit:** This enhancement expands the existing Shipment Group tendering functionality by introducing additional tender agent actions that support more complete automation of the Shipment Group tender workflow. You can now automate key shipment group tender lifecycle activities using configurable agent actions instead of relying on more manual operational processing.

## ⚙️ Steps to Enable and Configure

To take advantage of the Shipment Group tender related Agent Actions, you will need to add or update an existing Shipment Group Agent Type automation agent  to use the new Shipment Group tender agent actions:

• **TENDER SHIP GROUP**
• **ACCEPT SHIPMENT GROUP TENDER**
• **WITHDRAW SHIPMENT GROUP TENDER**
• Optionally configure Decline Reason Code handling for your withdrawal scenarios as needed by your business process.

Shipment Group Tender Agent Actions

## 💡 Tips and Considerations

• Review existing automation agent configurations to identify opportunities to replace manual processing steps with automated actions.
• Use decline reason codes consistently to improve operational reporting and exception analysis.
• Validate downstream workflows that may depend on shipment group tender acceptance or withdrawal status updates.
• Ensure operational users understand how automated acceptance and withdrawal processing may affect existing exception handling procedures.

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*