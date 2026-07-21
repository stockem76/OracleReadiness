[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Service Center](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/service-center.md)

# Differentiate Contacts vs Partner Contacts in the Service Request Contacts Table

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/bsvc-26c/26C-b2b-service-wn-f47302.htm)

In the Service Request (SR) Details page, the Contacts table (which appears from the "Show Contacts" smart action) includes a new **Contact Type** column, allowing users to more easily identify the type of contact directly within the list view.

By adding the ContactTypeCd field to the table layout using Visual Builder Studio, users can easily see whether a record represents a Contact or a Partner Contact without relying on navigation links.

This improvement increases clarity and reduces user confusion when managing multiple contact types within a service request. It helps agents quickly identify the right contact, improves efficiency in customer interactions, and minimizes errors when selecting or referencing contacts

## ⚙️ Steps to Enable and Configure

Contact Type Column

### **Steps to Enable**

1. Navigate to **VB Studio**.
2. Go to **Layouts** > **Customer Experience (CX)** > **Service Center** > **Service Requests** > **Contacts**.
3. Locate the Contacts layout and select the dynamic table: **Service Request Details Contact Layout**.
4. Duplicate the layout to create a custom version.
5. In the duplicated layout, add the field **ContactTypeCd** as a new column.
6. Save and **Preview** the changes.

Once completed, the Contacts table will display a new column indicating the contact type, making it easier to differentiate between Contact and Partner Contact records.

## 💡 Tips and Considerations

n/a

## 🔐 Access Requirements

• Oracle Visual Builder Studio for Fusion Application Extension

## 📚 Key Resources

n/a

---
*Oracle Cloud Readiness · 26C · SERVICE · Service Center*