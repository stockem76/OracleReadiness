[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# AI Agent: Inbound Goods Advisor

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f46496.htm)

Cross-Docking enhances your warehouse efficiency by reducing the number of steps required for personnel to fulfill outbound demand. In Oracle Fusion Cloud Advanced Inventory Management, the existing cross-docking functionality alerts you to potential opportunities and helps you to move goods to the outbound staging area. However, it doesn't automatically associate those goods with specific outbound demand or update the demand status.

The Inbound Goods Advisor AI Agent addresses this gap by identifying cross-docking opportunities and automatically execute the necessary fulfillment steps to ensure that outbound demand is properly staged and is ready for shipment. Additionally, for goods that are not eligible for cross-docking, the Inbound Goods Advisor AI Agent recommends optimal put away locations based on historical transaction data or, when such data is limited, existing put away prioritization rules.

To access the Inbound Advisor AI Agent:

1. Navigate ot the **Tools** menu, and then click **AI Agent Studio**.
2. Search by product family, product or agent template name and description.
3. Copy the seeded template by clicking on the **Copy Template**button. When copying the template, you can specify an agent team suffix. The newly copied template will be available to search under the Agent Teamstab.

AI Agent: Inbound Advisor

The Inbound Advisor combines two separate AI Agents - the Inventory Cross Dock Advisor and the Put Away Advisor. You can run these two AI Agents independently. For example, you may want to run the Inventory Cross Dock Advisor to only generate cross-dock suggestions. If you are only interested in put away suggestions, you can run the Put Away Advisor AI Agent separately.

Agent Teams

Typically, you may schedule the Inbound Advisor to run on a scheduled interval. For example, to run every hour. The Inbound Advisor will use expected inbound supply, receipts, and outbound demand to suggest cross-dock opportunities. Additionally, the Inbound Advisor can be scheduled to identify the suggested put away location for the received material.

Schedule Trigger

You can invoke the Inbound Advisor by entering a prompt for use cases where you want to run the Inbound Advisor between scheduled intervals. For example, you have received a rush item and you want to fulfill eligible cross-dock demands. You can enter a prompt, such as **Generate suggestions for receipt 33914 in organization M1**. Clicking the **Arrow** icon will submit your request. After the Inbound Advisor completes, a confirmation message will be displayed indicating that both cross-dock and put away suggestions completed successfully.

These are the sample prompts you can use while submitting the Inbound Advisor:

• ***Generate suggestions for receipt 33914 in organization M1.***
• ***Regenerate suggestions for receipt 33914 in organization M1.***
• ***Regenerate the put away suggestions for organization M1 and receipt 456.***
• ***Generate the suggestions again for put away in organization M1 and receipt 456.***
• ***Regenerate put away suggestions. Organization M1. Receipt 456.***

Cross-docking is supported for both opportunistic and planned cross-docks. Opportunistic cross-docking matches material that has been received with demand. Whereas, planned cross-docking matches incoming supply yet to be received with demand.

Inbound Advisor Prompt

The reservations process flow has been enhanced to support cross-docking. A reservation automatically created when a cross-dock demand document is matched against a cross-dock supply document. A new Cross-Dock Enabledcolumnhas been introduced for you to easily identify cross-dock specific reservations. The Include existing reservations advanced inventory parameter can be enabled to include existing reservations for cross-dock processing. You can also update and delete cross-dock reservations. Lastly, the cross-dock indicator will be removed when the reservation is transferred from the supply document to on-hand.

Cross-Dock Reservations

The Receiving Transaction History page has been enhanced to display cross-dock specific information. The Cross-Dock Order Type, Cross-Dock Order Number, and Cross-Dock Order Line,are the newly added columns to get information about the receiving transactions associated with cross-dock demand documents.

Receiving Transaction History

After running the Inbound Advisor, you can navigate to the Put Away Goods mobile page and search for your receipt number. An informational note will be displayed on the item card indicating that cross-docking suggestions are available. After you click on the item card, you can review the cross-dock suggestions. The cross-dock suggestions will show the suggested subinventory, item and quantity, and associated demand document. Items to be cross-docked will be moved to a staging subinventory to fulfill outbound demand, such as a sales order or transfer order.

Scenarios where you want to bypass cross-docking for selected orders, for example, goods might be damaged and you want to exclude the order form cross-docking. In such cases, you can select multiple items, and then click on the **Exclude from Cross-Dock** button or you can exclude a single item from cross-docking by selecting the **Exclude from cross-dock**checkbox. To exclude from cross-dock. administrators need to provision the Exclude Demand Document from Cross-Dock privilege for the appropriate users.

The privilege Exclude Demand Document from Cross-Dock (AIM_EXCLUDE_DEMAND_CROSS_DOCK_PRIV) must be assigned to a configured job role to access action Exclude from Cross-Dock.

Cross-Dock Suggestions

After you have completed the put away to the staging subinventory, the shipment lines will be in Staged status  and are ready for shipment. You can navigate to the Ship Goods page to complete the shipment.

Ship Cross-Dock Orders

The Inbound Advisor generates put away suggestions based on historical transaction data and user-configurable rules. The agent will suggest the optimal put away location based on the most recent put away transaction or the most frequent put away location. For example, when you perform put away transaction, the agent uses item, organization, document type, and supplier attributes to determine the appropriate put away location. In addition to historical transactions, put away suggestions can also be generated based on the user-configurable rules defined in the Advanced Inventory Parameters page.

Put Away Suggestions

This feature improves operational efficiency by giving you greater visibility into potential cross-docking opportunities, enabling you to execute them without multiple manual steps, and suggesting the optimal put away location when goods are not eligible for cross-docking.

*Here's the demo of these capabilities:*

## ⚙️ Steps to Enable and Configure

**Configure Advanced Inventory Parameters**

To enable cross-docking, you must select the **Cross-Dock Action**on the **Advanced Inventory Parameters**setup page.

Navigate to the Setup and Maintenance work area and select task Advanced Inventory Parameters under the Advanced Inventory Management functional area.

**Cross-Docking**

• Select the **Cross-Dock Action**
• None
• Notification only: Provides cross-dock notifications only. You can review feature Redwood: Notify Users of Cross-Docking Opportunities for additional details.
• Process cross-dock: Uses AI Agent to identify and process cross-dock suggestions.
• Include existing reservations; Includes existing reservations when performing cross-dock.
• Include expected supply: Includes expected supply when performing cross-dock. This parameter is used for planned cross-docks when material has yet to be received.
• Supply Expected Days; Number of supply expected days. This parameter is used for planned cross-docks when material has yet to be received.
• Cross-Dock Item Category: Item category used to identify goods eligible for cross-docking.
• Demand Due Days: Number of days used to evaluate outbound demand awaiting shipment.
• Due Date Sort: Sorts demand based on ascending or descending due date.
• Include backorders: Includes backorders when performing cross-dock.

**Put Away Suggestions**

• Select the **Put Away Action**
• None
• Use Basic Rules: Uses priorities including A specific zone, A specific subinventory and locator, Item subinventory and locator association, and Where on-hand already exists. You can review feature Redwood: Suggest a Put-Away Location for Goods for additional details.
• Use Advanced Rules - Uses AI Agent to intelligently identify put away suggestions based on historical put away transactions.

Advanced Inventory Parameters

## 💡 Tips and Considerations

• Cross-docking isn't supported for purchase orders with multiple distributions
• Cross-docking isn't supported for non-reservable and non-shippable items
• Cross-docking doesn't include Kanban and PAR replenishment requests as inbound supply
• Planned cross-docking suggestions are removed in case of partial receipt of supply document
• Cross-docking isn't supported for work order demand and movement request demand
• The action to Exclude from Cross Dock is only available if the user is provisioned the privilege Exclude Demand Document from Cross-Dock (AIM_EXCLUDE_DEMAND_CROSS_DOCK_PRIV)

## 🔐 Access Requirements

To access the Oracle AI Agent Studio for Fusion Applications and manage SCM AI agents, users must be assigned a configured job role that contains these duty roles:

• SCM Intelligent Agent Management Duty (ORA_RCS_SCM_AI_AGENT_MANAGEMENT_DUTY)
• SCM Intelligent Agent Management Duty (ORA_RCS_SCM_AI_AGENT_MANAGEMENT_DUTY_HCM)
• Fai Genai Agent SCM Administrator Duty (ORA_DR_FAI_GENERATIVE_AI_AGENT_SCM_ADMINISTRATOR_DUTY)

To interact with AI agents in product pages, users must be assigned a configured job role that contains this duty role:

• Fai Genai Agent Runtime Duty (ORA_DR_FAI_GENERATIVE_AI_AGENT_RUNTIME_DUTY)

In the Security Console, filter by Roles and Permission Groups to find this duty role.

To allow users to interact with agents, you must also enable permission groups in the Security Console on those users' configured job roles that contain the Fai Genai Agent Runtime Duty role. You can enable permission groups when you manage the basic information of your configured job roles.

Users' configured job roles must also contain privileges that allow access to the pages where AI agents are enabled.

See Access Requirements for AI Agent Studio (for administrators) and How can I give users access to AI agents (for end-users) for more information.

To set up this feature, you'll need a configured job role that contains this new duty role, which is not assigned to any predefined job roles:

• Advanced Inventory Management Administration Duty (ORA_INV_ADVANCED_INVENTORY_MANAGEMENT_ADMINISTRATION_DUTY)

This duty role was available prior to this update.

To interact with the Inbound Advisoragent, users must be assigned a configured job role that contains this privilege:

• Access Inbound Advisor Agent (AIM_ACCESS_INBOUND_ADVISOR_AGENT_PRIV)

This privilege is new in this update.

To access the action Exclude from cross-dock, users must be assigned a configured job role that contains this privilege:

• Exclude Demand Document from Cross-Dock (AIM_EXCLUDE_DEMAND_CROSS_DOCK_PRIV)

This privilege is new in this update.

## 📚 Key Resources

• Oracle Fusion Cloud SCM: Using Inventory Management guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.
• Access Requirements for AI Agent Studio
• How can I give users access to AI agents?
• Create AI Agents

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*