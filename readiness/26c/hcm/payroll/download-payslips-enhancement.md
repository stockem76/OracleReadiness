[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# Download Payslips Enhancement

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f46590.htm)

The Download Payslips flow is enhanced to provide flexible submission options, enabling organizations to control how payslip access is secured. You can now choose to run the flow either as a **System Elevated User** or as a **Logged-in User**:

1. System elevated user:  
  • Any user with access to the flow can run it
• No additional data-level security is enforced
2. Logged-in user:  
  • Users can only access payslips they are authorized to view
• Data security is enforced based on the assigned Data Security Profiles (DSPs), such as LDG security, PSU, TRU, Person, and Payroll.

This enhancement improves data security and ensures controlled access to sensitive payroll documents.

## ⚙️ Steps to Enable and Configure

To submit the **Download Payslips** flow as a logged in user:

1. Navigate to **My Client Groups > Payroll > Payroll Flow Patterns**.
2. Search for the **Download Payslips** flow pattern.
3. Select the appropriate **Legislative Data Group** (LDG).
4. Edit the flow pattern.
5. Select the **Submitting User** checkbox.
6. Save your changes.

## 💡 Tips and Considerations

• Use the **Logged-in User** option to enforce data security and restrict access based on user roles and DSPs.
• Use the **System Elevated User** option for administrative scenarios where unrestricted access is required.
• Ensure that appropriate DSPs are configured for accurate access control.
• Assign the Payroll Manager role to users who need to run the flow securely with data restrictions applied.

## 🔐 Access Requirements

To ensure that users can securely access and download payslip documents based on their authorization, they should have the following privileges:

• Payroll Manager role (recommended)
• Required privileges:  
  • ORA_PER_MASS_DOWNLOAD_DOCUMENT_RECORDS
• ORA_PER_VIEW_PERSON_DOCUMENTATION

## 📚 Key Resources

For more information, see:

• Administering Payroll Flows
• How do I set up payroll flows?
• Overview of Online Payslip

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*