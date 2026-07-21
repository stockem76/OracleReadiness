[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Order Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/order-management.md)

# AI Agentic App: Sales Order Command Center

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/order26c/26C-order-mgmt-wn-f46432.htm)

The new Sales Order Command Center is an AI-powered unified workspace that will improve customer satisfaction by giving Customer Service Representatives a simple way to continuously review sales order exceptions, review sales orders on hold, and coordinate and execute priority actions to drive faster issue resolution.

**Get these benefits**

• Review an AI-generated summary that highlights critical sales order exceptions, such as items on backorder and items failing in inventory reservation, and the recommended actions.
• Review Priority Actions to see the most critical sales order exceptions and take the recommended actions.
• Use Ask Oracle to cancel an entire order or cancel a line.
• Use Ask Oracle to return an entire order or return a line.
• Use Ask Oracle to apply and release holds on an order.

**How it works**

To open the Sales Order Command Center, go to **Order Management** > **Show More** > **Sales Order Command Center**.

Notice the Command Center action link conveniently located under the Order Management heading with all your other tools.

This is the exceptions page to view exception details.

Expand the Exceptions panel to view orders in exceptions and to view details of these exceptions.

Customer Service Representatives can resolve the following exceptions:

• Items on backorder
• Inventory reservation failure

Select the **Apply Recommendation** button in the Priority Actions panel to accept the recommendation without viewing details.  Select **View Details** to review details of the exception, the customer preferences, and alternate resolutions.

Select **Apply Recommendation** to apply the resolution recommended by the agent. Or you can select **Modify** to view alternate recommendations.

In the case of backorder exceptions, you are given the following recommendations, including a recommended option based on customer ordering preferences.

• Ship available
• Available quantity is shipped; the remaining quantity is shipped when available.
• Substitute Item
• Substitute with an equivalent item that is available in stock and that meets delivery window
• Ship from an alternate fulfilment location where inventory is available

In the case of inventory reservation exceptions, you will be given the following recommendations, with one of them as a recommended option based on customer ordering preferences.

• Reserve available and remaining later
• Available quantity is reserved; the remaining quantity remains in Manual Reservation Required status
• Reserve available quantity
• Available quantity is reserved and the remaining quantity is cancelled.
• Cancel line

**Cancel Order**

Cancel an order using Ask Oracle. Type the cancel order prompt or use your computer microphone to Ask Oracle to cancel your order. Provide a cancel reason in your prompt if you know the reason for cancellation.

The agent uses fuzzy matching to determine the exact cancel reason based on the reason provided in the prompt. If no reason is provided, a cancel reason is defaulted.

Return items that are not eligible for cancellation. Select **Cancel and Return**action to create the return order.

**Return Order**

Return an order using Ask Oracle. Type details in the return order prompt, or use your computer microphone to Ask Oracle to return your order. Provide a return reason in your prompt if you know the reason.

The agent uses fuzzy matching to determine the exact return reason based on the reason provided in the prompt. If no reason is provided, a return reason is defaulted.

**Apply Hold and Release Hold**

Use natural language to apply a hold on an order or release a hold on an order.  Provide hold comments if you want.

The agent performs a fuzzy match on hold names based on the hold name provided and prompts user to select the hold they want to apply.

**Select** the hold to apply on the order.

Confirm by selecting the **Apply Hold** action. The agent displays a message indicating that a request has been submitted to apply the hold.

Use natural language to release hold on the order.

Use the Release Hold action to submit a request to release the hold.

## ⚙️ Steps to Enable and Configure

To use this feature, the first thing you need to do is enable the Sales Order Command Center Agentic App Enabled profile option at the site and user level.

ORA_FOM_COMMAND_CENTER_AGENTIC_APP_ENABLED

Set the value of the profile to Y.

Once the profile is enabled, you will setup your crawler agent to look for issues. The agentic app consists of multiple autonomous workflow AI agents that periodically scan the order management sales order data to identify new or unresolved exceptions. The Sales Order Precompute Processor agent periodically crawls the transactional order data and policy documents to identify the exceptions.

**How to schedule your sales order crawler agent**

1. Schedule your crawler agent in AI Agent Studio. Go to **Tools** > **AI Agent Studio**, and search for the Sales Order Precompute Processor agent.
2. Select **Use Template** to create a new instance of your crawler agent.

1. Give your new agent a team name and select **Update**.

1. Select the **Schedule** icon > **Triggers** tab  > **Add** to schedule your agent at a defined time interval.

1. Select **Schedule Type** > **Interval**.
2. Select an **Interval Type** and enter the **Interval Between Hours**.
3. Enter a **Start Time**. You can also set an **End Date** and **End Time**
4. Select **Update**.

## 💡 Tips and Considerations

• Use a RAG document to provide details for the following information:
• Customer details such as Account Type, Annual Revenue, Sales Agreement, Penalty Clause, and Penalty.
• Order History Pattern such as Substitutes Accepted, Splits Accepted, Delay Tolerance, Average Orders Per Quarter, Average Order Value and whether the customer prefers Reserve Available option in case of reservation exceptions.
• The number of days to look back for orders containing exceptions.
• Matrix containing return reason and corresponding return types
• A default return reason that is used if a reason is not provided in the user prompt.
• A default return type
• A default cancel reason that is used if a reason is not provided in the user prompt.
• Cancel order action is supported for orders containing standard products only. Other item types are not supported.
• Return action is supported for the entire quantity. Partial quantity returns are not supported.
• Return order creation through the Sales Order Command Center is limited to standard products. ATO, PTO, kits, associated coverages, subscriptions, and non-shippable items are outside the documented scope.
• Apply hold action applies hold on all eligible lines of the order. The app does not support apply hold action on an individual line.
• Release hold action releases hold from the entire order. The app does not support release hold action on an individual line.
• Review AI recommended priority actions for accuracy before applying. Always validate AI suggestions against your business priority.
• You can’t access the sales order details from the Sales Order Command Center. To view sales orders details, log in to the Oracle Order Management work area on Redwood.

## 🔐 Access Requirements

Users who are assigned the job role below can access this feature:

• ORA_FOM_ORDER_ENTRY_SPECIALIST_JOB
• ORA_DOO_ORDER_MANAGER_JOB

If you have created custom job roles, you can assign the following duty role to your custom job roles.

• ORA_DR_FOM_SO_COMMAND_CENTER_WORKFLOW_DUTY

## 📚 Key Resources

Building Agentic Apps Using Agents from AI Agent Studio

---
*Oracle Cloud Readiness · 26C · SCM · Order Management*