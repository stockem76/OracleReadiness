[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Help Desk](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/help-desk.md)

# Create Cases from AI Conversations with the Case Creation Agent

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/shde-26c/26C-helpdesk-wn-f47324.htm)

The Case Creation Agent can create Cases easily from within any AI interaction, assessing the user's input and assigning appropriate values for core Case fields including Title, Description, Category and Primary Contact as well as grievance and disciplinary action related fields (if applicable).

The Case Creation Agent provides a new style of user interaction, able to create a new Case based solely on the content of a simple chat-style AI conversation. The output of the Case Creation agent can be used within AI chat conversation UI, AI Agent team workflows, and Visual Builder user applications.

## ⚙️ Steps to Enable and Configure

The Case Creation Agent is seeded in AI Agent Studio as a runnable agent, allowing uptake of this agent by any new/existing AI agent team or any Visual Builder application.

The Case Creation Agent can operate in two different modes (based upon the value of the 'returnCasePayload' parameter):

1. 'returnCasePayload' = false: a Case is created, a confirmation message is returned with Case number and title.
2. 'returnCasePayload' = true: a formatted JSON payload is returned.

Finally, the Case Creation Agent will also merge additional field values provided as input in  'additionalAttributes' and 'attachedDocumentIDList'.

## 💡 Tips and Considerations

When creating a Case, **the Case Creation Agent Agent considers the user's input and recent AI chat history to create a Case**:

**For all Cases:**

• **Stripe:**Derived from the conversation context (if not provided as input).
• **Title and Description:** Derived from the conversation context.
• **Type**: Derived from the conversation context.  Possible values: Grievance, Disciplinary Action or None,
• **Case Category:** Determined via the 'Service Request Category Agent' (for details refer to this agent in AI Agent Studio for more details).
• **Primary Contact:** Identified from the context, if possible; defaults to the *Logged-in User PartyID* if no specific contact can be identified.

**Additionally, for when Case Type is 'grievance' or 'disciplinary action':**

• **Grievance Cases:** *Incident Type, Incident Occurrence Date, Allegation*.
• **Disciplinary Action Cases:** *Incident Occurrence Date, Measures Taken,* and *Reviewed By*.

## 🔐 Access Requirements

The Case Creation Agent uses the roles, privileges and access grants of the user it is interacting with.

## 📚 Key Resources

To learn more about AI Agent Studio, consider these resources:

1. 'Oracle AI for Fusion Applications' (documentation)
2. 'Introduction to AI Agents in Oracle Cloud HCM and SCM' (recorded presentation, account required)
3. 'Oracle AI Agent Studio for Fusion Applications Foundations Associate' (training and certification, account required)

---
*Oracle Cloud Readiness · 26C · SERVICE · Help Desk*