[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [ERP](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/index.md) › [Project Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/erp/project-management.md)

# Project Billing and Revenue Event Creation Assistant

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/ppm26c/26C-ppm-wn-f49410.htm)

Helps users create recurring invoice and revenue events for eligible external fixed-price contracts through a guided conversational experience.

The assistant validates the contract or contract line, billing frequency, event type, contract line dates, contract line amount, and existing event details. It then calculates the proposed event dates and amounts, presents a preview for review, and creates the events only after the user confirms.

Use the Project Billing and Revenue Event Creation Assistant to:

• **Create recurring invoice and revenue events** for external fixed-price contracts or contract lines, with frequencies of monthly, quarterly, half-yearly, or yearly.
• **Preview proposed events**before creation.
• **Update proposed event attributes** before creation, such as description, completion date, amount, organization, transaction task, invoice or revenue hold.
• **Identify missing or unsupported contract details**that prevent event creation.

**Example Flow**

Maria, a project billing specialist, is reviewing an external fixed-price contract and needs to create recurring billing and revenue events for a contract line. Instead of manually calculating event dates and amounts, she uses the assistant to generate events through a guided conversational flow.

Maria opens the assistant and provides relevant details for the **contract**, **contract line**, **event type**, and **frequency**.

The assistant confirms the entered details with Maria, and then validates the contract, contract line, event type, billing frequency, contract line dates, contract line amount, and existing event details.

Provide Event Creation Details

After validation is complete, the assistant calculates the proposed recurring event schedule based on the contract line duration and amount. It then displays a preview of the events to be created, including the event dates, completion dates, event amounts, descriptions, project or task details, and invoice or revenue hold values.

Preview Proposed Events Before Creation

Maria reviews the proposed events. If any supported attribute needs to be changed, she can ask the assistant to update it before it creates the events. For example, Maria asks the assistant to modify the invoice hold attribute to 'Yes' for the month of September-2026.

The assistant updates the preview and asks Maria to confirm whether the proposed events should now be created. Maria reviews the final preview and confirms.

Modify Event Attributes

The assistant creates the recurring invoice and revenue events only after receiving confirmation. It then displays a success message with the created event details, helping Maria complete the billing and revenue setup without manually entering each recurring event.

If the selected contract line isn’t eligible, the assistant explains why the events can’t be created. For example, it may indicate that the contract line doesn’t have a valid end date, has a zero amount, uses an unsupported billing frequency, or already has recurring events.

Create Events After User Confirmation

The benefits of this feature are:

• **Accelerates billing and revenue event creation** by automatically generating recurring events.
• **Reduces manual effort**by calculating event schedules and amounts based on the contract line duration, amount, and selected billing frequency.
• **Improves accuracy** through validation of contract details, contract lines, event types, billing frequency, and eligibility criteria before event creation.

## ⚙️ Steps to Enable and Configure

**Project Billing and Revenue Event Creation Assistant**role is needed to use the assistant within the AI Agent Studio. Refer to the Access Requirements section for details.

**NOTE:** The Project Billing and Revenue Event Creation Assistant is a preconfigured template. You need to create your own agent using the preconfigured template. To learn how to set up AI agents, see Create AI Agents Using Preconfigured Agent Team Templates.

## 💡 Tips and Considerations

Keep these points in mind when using the assistant:

• The assistant supports recurring billing and revenue recognition for external fixed-price contracts and contract lines. Item-based recurring billing events aren’t currently supported.
• Users must provide the exact contract name or number, contract line name or number, and event type, as partial values aren’t supported.
• Supported billing frequencies include Monthly, Quarterly, Half-Yearly, and Yearly.
• Recurring events can only be created when the contract line has a valid end date and a non-zero contract line amount.
• If recurring events already exist for a contract line, the assistant notifies the user and prevents duplicate event creation.
• Depending on the contract line amount and required event frequency, minor rounding differences in event amounts may occur, which might require manual adjustment.
• Currently only English is supported as an input language.

## 🔐 Access Requirements

To access the **Project Billing and Revenue Event Creation Assistant**, users must be assigned the predefined **Customer Contract Administrator** and **Project Billing Specialist**roles, or a custom role copied from these predefined roles.

The custom role needs to have the following configurations:

**a) Function Security Policies > Privileges**

Add the following functional privileges:

• View Contract (**OKC_VIEW_CONTRACT_PRIV**)
• Manage Project Billing Event **(PJB_MANAGE_PROJECT_BILLING_EVENT_PRIV)**
• Maintain Project Contract Revenue**(PJB_MAINTAIN_PROJECT_CONTRACT_REVENUE_PRIV)**

**b)Data Security Policies**

• **Grant on Business Unit**
• **Data Resource:** Business Unit
• **Actions:** Manage Project Billing Event
• **Condition:** Access the business units for which the user is explicitly authorized

**c)** **Role Hierarchy > Roles and Privileges**

  Add the following duty roles:

• Project Contract Invoice Management **(ORA_PJB_PROJECT_CONTRACT_INVOICE_MANAGEMENT_DUTY)**
• Project Contract Revenue Management **(ORA_PJB_PROJECT_CONTRACT_REVENUE_MANAGEMENT_DUTY)**

1. In the **Basic Information** section of the predefined or custom role, ensure that the **Enable Permission Groups** option is selected.
2. Navigate to **Permission Groups**section and add the following permission group: 
  • **read:Project Contract Billing Event Type** (oraErpCoreProjectCommonSetup_ProjectContractBillingEventType_read)
• Set the **Security View** to '**All Rows and All Fields**'
3. The user must have the appropriate **Resource Role** and **Organization** setup in **Manage Users** to access contracts in the relevant business unit(s).

Associate the predefined or custom role with the agent team using a user with administrator access.

1. Navigate to **Navigator > Tools > AI Agent Studio**.
2. Open the **Agent Teams** tab and edit the agent team for which you want to grant user access.
3. Click the **Agent Team Settings** icon and open the **Security** tab.
4. Add the predefined or custom role.
5. Apply the changes, then update and publish the agent team.

Agent Team Security

## 📚 Key Resources

• Explore AI Agents for Oracle Fusion Cloud Applications
• How do I use AI Agent Studio?

---
*Oracle Cloud Readiness · 26C · ERP · Project Management*