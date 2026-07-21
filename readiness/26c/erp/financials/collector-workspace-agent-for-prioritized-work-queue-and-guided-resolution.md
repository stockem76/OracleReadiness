[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Financials](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/financials.md)

# Collector Workspace Agent for Prioritized Work Queue and Guided Resolution

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49306.htm)

The Collector Workspace introduces an AI-powered collections experience that helps organizations improve collector productivity, accelerate cash recovery, and drive more consistent customer engagement.

The Collector Workspace Agent transforms collections from a manual, fragmented, and search-intensive process into an AI-driven, prioritized, and action-oriented experience. It helps collections teams quickly identify the customer accounts that require attention, understand the factors driving urgency, and take the next best action from a unified workspace.

Collections teams often need to review customer and receivables information across multiple systems before engaging with a customer or completing an internal review. Critical context such as invoices, disputes, payment history, promises to pay, and information captured from incoming customer emails may be distributed across various systems and email channels. This fragmentation makes it difficult for collectors to quickly understand the full account context, identify the reason for non-payment, and determine the right follow-up action.

With the Collector Workspace Agent, collectors can access key customer and receivables insights in one unified experience. The agent uses governed collections policies and AI-driven reasoning to prioritize accounts, explain urgency drivers, summarize account context, and recommend policy-aware next-best actions. This enables collectors to work from a more complete and consistent understanding of each customer, respond faster, and make more informed decisions.

**Key Capabilities**

• **AI-Prioritized Customer Worklist -**Provides collectors with a ranked list of customer accounts that require attention, guided by governed collections policies. The worklist surfaces the key priority drivers behind each account, helping collectors quickly understand what needs attention, why it matters, and where to focus first.
• **Customer Drilldown and Account Context Summary -**Enables collectors to drill into a specific customer account and view a consolidated summary of receivables status, prior activity, payment history, disputes, promises to pay, and recommended next steps.
• **Next-Best Action Recommendations -**Recommends policy-aware next actions based on account context and collections priorities, such as requesting promise to pay or calling customers.
• **Conversational Account Inquiry -** Enables collectors to ask natural-language questions about customer accounts, such as open invoices, disputes, payments, and promises to pay, and receive contextual answers without navigating across multiple screens.
• **Incoming Email Intelligence -** Extracts and summarizes key details from incoming customer emails, helping collectors quickly identify customer intent and required follow-up actions, such as promises to pay, disputes, invoice copy requests, and purchase order updates.
• **Customer Communication Drafting -**Assists in drafting policy-aware customer emails and follow-up messages using available account context, prior activity, incoming email details, and recommended actions.
• **Collections Activity Support -**Helps collectors complete common collections activities such as surfacing collection call scripts, creating call notes, capturing promises to pay, and recording disputes.
• **Policy-Governed Guidance -** Uses governed collections policies to support consistent prioritization, recommendations, communications, and collector actions across customer accounts.

**Collector Workspace Experience**

The Collector Workspace Agent provides a focused collections experience through two primary views that help collectors prioritize customer accounts, understand account context, and take timely action.

**Prioritized Customer List:**Collectors can start their day with a ranked list of customer accounts that require attention. The list is driven by policy-defined prioritization signals such as overdue balances. For each customer, the workspace highlights the key priority drivers and recommends the next best action, helping collectors decide where to focus first and what to do next.

Collector Workspace- Prioritized Customer List

**Customer Drill-Down**: Collectors can drill into a specific customer account to get a complete view of the collection context in one place. This includes aging, overdue balances, prior Collections activity, and recommended next steps. This detailed view helps collectors engage customers with the right context, make faster decisions, and act without switching between multiple systems.

Collector Workspace- Customer Detail

The Collector Workspace Agent delivers measurable business value by accelerating cash recovery, improving collector productivity, standardizing collections execution, and enhancing customer engagement through AI-driven insights and automation.

• **Accelerated receivables recovery** - Helps collectors focus on the highest-priority accounts first, take timely follow-up actions, and reduce delays in cash collection.
• **Higher collector productivity** - Reduces time spent searching across multiple systems and streamlines routine collections activities, such as reading incoming customer emails to identify intent and follow-up actions, and drafting responses based on customer context. This enables collectors to spend less time on administrative work and more time on value-added recovery activities.
• **Consistent, policy-driven execution** - Applies business-defined prioritization rules, so collectors focus on accounts based on risk, urgency, exposure, and collection impact.
• **Improved customer experience**- Equips collectors with complete and accurate context, enabling faster responses, clearer communication, and fewer repeated information requests.
• **Better business decisions** - Uses AI-driven insights and account-level collections data to recommend next best actions and support informed, policy-aligned decisions.
• **Lower operational risk**- Reduces errors from manual data gathering and inconsistent processes, helping teams follow standardized collections practices.
• **Stronger cash flow visibility**- Gives collections teams a clearer view of outstanding receivables, high-priority accounts, payment commitments, and disputes, improving visibility into collection priorities and cash flow impact.

## ⚙️ Steps to Enable and Configure

• Pre-Requisite: Analytical Views must be enabled.
• Use the Collections Policy Execution Assistant to upload the policy for use in the Collector Workspace. For information about access to this assistant, refer to the Access Requirements section.
• To use the incoming email intelligence capability, associate the email account with the Collections Email Response Assistant in AI Agent Studio so that incoming emails can be read and processed. For details on adding email accounts, refer to Add Email Accounts.
• Collections Workspace Assistant role is needed to use the Collector Workspace Agentic Application within the AI Agent Studio. Refer to the Access Requirements section for details.

## 💡 Tips and Considerations

• The Collector Workspace doesn’t replace standard Receivables setup, approval rules, or dispute resolution processes.
• The information shown is based on customer account-level receivables data, including related transactions, receipts, disputes, promises, and activities.
• There is **no requirement to run Collections delinquency programs, including Refresh Receivables Transactions for Customer Balance and Delinquency Management,** before using the Collector Workspace.
• Collection priorities depend on the freshness and completeness of customer account, transaction, receipt, dispute, promise, and activity data.
• Aging and overdue balances depend on transaction due dates, payment terms, and open receivables data. **Currently, the following aging buckets are supported: Current, 1-5 days, 6 - 10 days, 11 - 30 days, 31 - 60 days, 61 - 90 days, over 90 days.**
• **Promise and broken-promise visibility depends on collectors consistently recording and updating promise-to-pay information and running the promise reconciliation program.**
• Workspace information reflects the state of application data at the time it’s viewed or refreshed.
• If receipts, disputes, promises, adjustments, or customer account data change after a work item is reviewed, users should refresh the application to get the latest snapshot.
• Sending dunning letters is not in scope for the Collector Workspace Agent. Existing dunning letter setups and processes should continue to be used.
• The workspace operates within the user’s existing Oracle Fusion security, data access, approval, and segregation-of-duties framework.
• Users can view and act only on customers, accounts, business units, and transactions they’re authorized to access.
• The workspace doesn’t bypass existing Receivables validations, dispute controls, approval rules, write-off controls, or customer account security.

## 🔐 Access Requirements

Use the following steps to provide users with access to the **Collector Workspace** and the **Collections Policy Execution Assistant**.

• **Scenario 1** - If You Have Implemented Custom Job Roles

Use these steps for users who aren’t assigned the Oracle-provided seeded **Collections Agent** or **Collections Manager**job roles. To enable access, create and assign a custom role with the required assistant duty role.

1. Navigate to the **Security Console**.
2. Search for the custom job role you want to use.
3. Click **Edit Role**.
4. Select **Enable Permission Groups**.
5. Save your changes.
6. Navigate to **Role Hierarchy > Roles and Privileges**.
7. Add the appropriate duty role: 
  • For access to the **Collector Workspace**, add the **Collections Workspace Assistant** duty role to your Collectors
• For access to the **Collections Policy Execution Assistant**, add the **Collections Policy Execution Assistant** duty role to your Collection Managers
8. Navigate to **Role Hierarchy > Roles and Permission Groups**.
9. Add the same duty role you added in the previous step: 
  • **Collections Workspace Assistant**
• **Collections Policy Execution Assistant**
10. Save your changes.

• **Scenario 2**- If You Have Used Oracle-Provided Seeded Job Roles

Use these steps for users who are assigned the Oracle-provided seeded **Collections Agent** or **Collections Manager**job roles. These users can access the corresponding workspace or assistant without additional role assignment:

• Users with the **Collections Agent** job role can access the **Collector Workspace**.
• Users with the **Collections Manager** job role can access the **Collections Policy Execution Assistant**.

Also, the following configuration must be completed:

1. Navigate to the **Security Console**.
2. Search for the applicable seeded job role, or the custom role derived from it: 
  • **Collections Agent**
• **Collections Manager**
3. Click **Edit Role**.
4. Select **Enable Permission Groups**.
5. Save your changes.

• **Data Access Requirements** for the Collector Workspace

Users must also have the appropriate data access for the business units, customer accounts, customers, and Receivables data they are expected to review. The Collector Workspace displays customer balances, transactions, promises, disputes, and activities only for the data the user is authorized to access. Use the **Manage Data Access for Users** task in the **Users and Security** functional area to assign users the appropriate data access based on their job roles.

Users will only see customer accounts for which they are assigned as collectors. Collector assignments are managed at the customer account profile level.

## 📚 Key Resources

• How do I use AI Agent Studio?
• Explore AI Agents for Oracle Fusion Cloud Applications
• Promise to Pay Overview
• Overview of Dunning

---
*Oracle Cloud Readiness · 26C · ERP · Financials*