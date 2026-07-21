[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Print Label Support to LPN Inquiry and RF Pallet Inquiry

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50169.htm)

Mobile LPN Inquiry and Pallet Inquiry transactions now support direct label printing from the inquiry screens, improving operational efficiency for warehouse users.

• Following new hot keys are introduced
• **CTRL-P: Print Label** in LPN Inquiry
• **CTRL-P: Print Pallet Label** in Pallet Inquiry

• For LPN Inquiry, users can scan or select a printer before initiating label printing, WMS uses the Label Rules Engine when configured, or defaults to the label template setup.
• The system records label print history in the Label Printing UI for tracking and audit purposes.
• For Pallet Inquiry, when users perform  CTRL-P : Print Pallet Label, the system validates pallet availability before printing and displays **No Pallet Found** if a pallet has not been scanned.
• Print initiation messages can be configured through Facility Message Configuration.

## ⚙️ Steps to Enable and Configure

1. Configure Label Rules Engine or label templates.
2. Review Facility Message Configuration for the label print initiation message.
3. Use **CTRL-P** from the **LPN Inquiry detail** screen.
4. For Pallet Inquiry, confirm printer setup for pallet label users.
5. Configure Label Rules Engine or pallet label templates.
6. Review Facility Message Configuration for the pallet label print message.
7. Scan a pallet before using **CTRL-P**.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*