[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Payroll](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/payroll.md)

# P45 Document Type in Document of Record (DoR)

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/payr-26c/26C-payroll-wn-f45876.htm)

Publishing P45 documents to an employee's document of record reduces reliance on paper distribution and centralizes access for leavers and payroll staff, improving record availability and traceability. This is important for payroll administrators and human resources teams who need reliable distribution options and auditable delivery methods.

Delivery preferences replace the previous output destination for P45s and control whether P45s are produced as Paper, Online (DoR), or both. By default the system produces Paper output only; delivery preferences can be set at organization, department, location, or person levels to change that behavior. When Online is selected the P45 is posted to DoR so it is available to the ex-employee and payroll roles. Email notifications for Online P45s are sent only when the environment lookup is enabled for email and the employee has a valid home email address. Paper and Online produces both DoR posting and inclusion in consolidated paper output; Paper-only produces no DoR posting.

• Delivery preferences replace the previous output destination for P45s and control whether P45s are produced as Paper, Online (DoR), or both.
• By default the system produces Paper output only; delivery preferences can be set at organization, department, location, or person levels to change that behavior.
• When Online is selected the P45 is posted to DoR so it is available to the ex-employee and payroll roles.
• Email notifications for Online P45s are sent only when the environment lookup is enabled for email and the employee has a valid home email address.
• Paper and Online produces both DoR posting and inclusion in consolidated paper output; Paper-only produces no DoR posting.

You can publish P45 documents to the person's document of record so leavers and payroll staff can access P45s online in addition to or instead of paper or email delivery. P45 delivery to document of record (DoR) centralizes document access and can reduce paper handling and distribution delays.

## ⚙️ Steps to Enable and Configure

1. Configure the new P45 document type in document of record.
2. Set delivery preferences at the organization-level Optionally, you can override by department, location, or person.
3. If you want email notifications for Online delivery, ensure the environment lookup controlling P45 email is set for your production pod and employee home email addresses are maintained.
4. Grant the temporary 'Leaver' role to any previous employees or otherwise provide them access to view P45s in DoR. Payroll administrator and payroll manager roles retain access without change.

## 💡 Tips and Considerations

• Delivery preferences are only evaluated in active runs. Test runs (rehearsals) always produce Paper output.
• Email sending requires two conditions: the environment-level lookup for P45 email must be enabled for your pod, and the employee must have a valid home email address.
• Lookup default behavior differs by run type: for active runs, if the P45 email lookup is missing email is disabled by default; for reprint runs the design indicates email may be enabled by default when the lookup is missing—confirm environment setting before relying on email.
• Ex-employees need the temporary Leaver role (or equivalent access) to view P45s on DoR; payroll administrator and payroll manager roles always have access.
• Selecting Online will post the P45 to DoR (central repository); selecting Paper and Online will also include the P45 in consolidated paper outputs.
• Customers must configure the new P45 document type and set delivery defaults; this is an administrative change and not automatic for existing users.

## 🔐 Access Requirements

• Grant the temporary 'Leaver' role to ex-employees (or otherwise provide access) so they can view P45s in DoR.
• Payroll administrator and payroll manager roles retain access to P45s in DoR without change.
• Environment-level lookup for P45 email must be enabled for the production pod to permit email notifications; employees must have a valid home email address for email notifications to be sent.

---
*Oracle Cloud Readiness · 26C · HCM · Payroll*