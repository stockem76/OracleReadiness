[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Supply Chain Collaboration](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/supply-chain-collaboration.md)

# Redwood: Migrate B2B Location Codes to Customer B2B properties

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/sccv26c/26C-sccv-wn-f46527.htm)

You can use a Redwood page to define and maintain location codes used to identify ship-to and bill-to locations when processing order-to-cash messages.

Here are the messages that support this feature:

• Purchase Order - Inbound
• Purchase Order Change - Inbound
• Purchase Order Cancellation – Inbound
• Purchase Order Acknowledgment - Outbound
• Purchase Order Change Acknowledgment - Outbound

You now have:

• **Reduced maintenance when addresses change**: When a physical address is updated, you maintain it only once in the customer site master data. Partners can continue using the same code without updating their message payloads.
• **Lower payload complexity**: Exchanging codes instead of full addresses can reduce verbosity and limit transmission of detailed location data.

## ⚙️ Steps to Enable and Configure

You can access this functionality by enabling the feature **Simplify Configuration and Processing for B2B Messaging**.

1. Perform the following standard steps to set up your documents:
1. Define your providers.
2. Configure your delivery methods.
3. Create connections.
4. Assign connections and properties to your documents.
5. Add customer messaging partner properties.

1. Follow these steps to set up and use your Messaging Location Codes:

1. Select **Partners** from the in-app navigation bar.
2. On the **Customer Messaging Properties** tab, select **Messaging Location Codes.**
3. On the Messaging Location codes page, select **Add**.
4. Enter the customer details. Note that the Site Number displays only customer sites that don’t already have a location code assigned. The Ship-to Site and Bill-to Site fields reflect the site’s defined address purposes.
5. Select **Create**.

Add a Messaging Location Code

1. As an alternative to adding location codes manually, you can import them using a .csv file.

The .csv file must include three columns with the following column headers (in any order):

Column Header | Description
CustomerNumber | Identifies the customer number
PartySiteNumber | Identifies the customer site number
LocationCode | Identifies the location code

1. 1. On the Messaging Location codes page, select **Import**.
2. Drag and drop the .csv file and select **Import**.

Import Location Codes

A message displays the scheduled process ID, which can be used to monitor the import status on the Scheduled Processes page.

Messaging Location Codes - Import request submitted message

1. To process a message like an inbound order, update the payload to include the required location codes at the Xpath locations specified in the table.

Original Message Payload

1. Once the message is processed, the transformed file will contain the expected values at the Xpath locations specified in the table.

Transformed Message Payload

**Xpaths to Include Location Codes in the Payload**

These paths correspond to the OAGIS10 Collaboration Messages.

Document | Header or Line Level on Order | Ship-To or Bill-To Code | XPath of Original Message | XPath of Transformed Message
PROCESS_PO_IN | Header level | Bill-to | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderHeader/BillToParty/Location/IDSet/ID[@typeCode="AccountSiteUseId"] | /Request/InboundCollaborationDocument/DOO_ORDERS/DOO_ORDER/DooOrderHeadersAllInt/DooOrderAddressesInt/AccountSiteUseId
PROCESS_PO_IN | Header level | Ship-to | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderHeader/ShipToParty/Location/IDSet/ID[@typeCode="PartySiteId"] | /Request/InboundCollaborationDocument/DOO_ORDERS/DOO_ORDER/DooOrderHeadersAllInt/DooOrderAddressesInt/PartySiteId
PROCESS_PO_IN | Line level | Bill-to | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderLine/Party[@role='BillTo']/Location/IDSet/ID[@typeCode="AccountSiteUseId"] | /Request/InboundCollaborationDocument/DOO_ORDERS/DOO_ORDER/DooOrderLinesAllInt/DooOrderAddressesInt/AccountSiteUseId
PROCESS_PO_IN | Line level | Ship-to | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderLine/ShipToParty/Location/IDSet/ID[@typeCode="PartySiteId"] | /Request/InboundCollaborationDocument/DOO_ORDERS/DOO_ORDER/DooOrderLinesAllInt/DooOrderAddressesInt/PartySiteId
CHANGE_PO_IN | Header level | Bill-to | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderHeader/BillToParty/Location/IDSet/ID[@typeCode="AccountSiteUseId"] | /Request/InboundCollaborationDocument/DOO_ORDERS/DOO_ORDER/DooOrderHeadersAllInt/DooOrderAddressesInt/AccountSiteUseId
CHANGE_PO_IN | Header level | Ship-to | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderHeader/ShipToParty/Location/IDSet/ID[@typeCode="PartySiteId"] | /Request/InboundCollaborationDocument/DOO_ORDERS/DOO_ORDER/DooOrderHeadersAllInt/DooOrderAddressesInt/PartySiteId
CHANGE_PO_IN | Line level | Bill-to | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderLine/Party[@role='BillTo']/Location/IDSet/ID[@typeCode="AccountSiteUseId"] | /Request/InboundCollaborationDocument/DOO_ORDERS/DOO_ORDER/DooOrderLinesAllInt/DooOrderAddressesInt/AccountSiteUseId
CHANGE_PO_IN | Line level | Ship-to | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderLine/ShipToParty/Location/IDSet/ID[@typeCode="PartySiteId"] | /Request/InboundCollaborationDocument/DOO_ORDERS/DOO_ORDER/DooOrderLinesAllInt/DooOrderAddressesInt/PartySiteId
CANCEL_PO_IN | Header level | Bill-to | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderHeader/BillToParty/Location/IDSet/ID[@typeCode="AccountSiteUseId"] | /Request/InboundCollaborationDocument/DOO_ORDERS/DOO_ORDER/DooOrderHeadersAllInt/DooOrderAddressesInt/AccountSiteUseId
CANCEL_PO_IN | Header level | Ship-to | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderHeader/ShipToParty/Location/IDSet/ID[@typeCode="PartySiteId"] | /Request/InboundCollaborationDocument/DOO_ORDERS/DOO_ORDER/DooOrderHeadersAllInt/DooOrderAddressesInt/PartySiteId
CANCEL_PO_IN | Line level | Bill-to | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderLine/Party[@role='BillTo']/Location/IDSet/ID[@typeCode="AccountSiteUseId"] | /Request/InboundCollaborationDocument/DOO_ORDERS/DOO_ORDER/DooOrderLinesAllInt/DooOrderAddressesInt/AccountSiteUseId
CANCEL_PO_IN | Line level | Ship-to | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderLine/ShipToParty/Location/IDSet/ID[@typeCode="PartySiteId"] | /Request/InboundCollaborationDocument/DOO_ORDERS/DOO_ORDER/DooOrderLinesAllInt/DooOrderAddressesInt/PartySiteId
ACKNOWLEDGE_PO_OUT | Line level | Ship-to | /processOutboundCollaboration/OutboundCollaboration/GetOrderDetailsResponse/Order/OrderLine/ShipToPartySiteIdentifier | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderLine/ShipToParty/Location/IDSet/ID[@typeCode="PartySiteId"]
ACKNOWLEDGE_CHANGE_PO_OUT | Line level | Ship-to | /processOutboundCollaboration/OutboundCollaboration/GetOrderDetailsResponse/Order/OrderLine/ShipToPartySiteIdentifier | CollaborationMessage/BusinessObjectDocument/DataArea/PurchaseOrder/PurchaseOrderLine/ShipToParty/Location/IDSet/ID[@typeCode="PartySiteId"]

## 💡 Tips and Considerations

• You can only import location codes by submitting the Import B2B Location Codes process from Messaging Location Codes.
• The system relies on specific XPath expressions to extract location codes. Ensure that incoming XML strictly follows expected structure.
• Ensure the correct typeCode is used. Any deviation will prevent code extraction. Here are the typeCodes:
• PartySiteId (Ship-to)
• AccountSiteUseId (Bill-to)

## 🔐 Access Requirements

Users who are assigned a configured job role that contains this privilege can access this feature: Manage B2B Trading Partners (CMK_B2B_TRADING_PARTNERS_PRIV).

This privilege was available prior to this update.

## 📚 Key Resources

Refer to the *Configuring and Managing B2B Messaging for Oracle Fusion Cloud SCM* guide on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Supply Chain Collaboration*