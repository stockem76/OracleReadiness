[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Service Center](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/service-center.md)

# Filter Recent Service Requests by Primary Contact for Improved Performance

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/bsvc-26c/26C-b2b-service-wn-f47316.htm)

In **26C**, a new extensibility option is introduced in the Service Contact page to improve performance when displaying Recent Service Requests.

Previously, the Service Contact Page retrieved all service requests where a contact was associated—either as a primary or secondary contact. This approach sometimes caused performance issues in environments with large data volumes, due to recursive queries across multiple contact relationships.

With this enhancement, you can enable a new option **“Show Recent SRs by Primary Contact”**, which limits results to only those service requests where the selected contact is the **primary contact**. Additionally, the system now restricts results to service requests updated within the **last 3 months**, further reducing query time.

This option uses a more efficient query based on **PrimaryContactPartyNumber**, improving response time and scalability.

• **Improved Performance:** Reduces query complexity and response time in high-volume environments
• **Better Scalability:** Handles large datasets more efficiently by avoiding recursive contact searches
• **Focused Results:** Displays only the most relevant service requests where the contact is primary

## ⚙️ Steps to Enable and Configure

Leverage the Visual Builder Studio to expose your applications. To learn more about extending your application using Visual Builder, visit Oracle Help Center > *your apps service area of interest* > Books > Configuration and Extension.

**Steps to Enable**

1. Open **Oracle Visual Builder Studio**
2. Navigate to: **Service Center > service > ec > sr > svc-contact page**
3. Go to the **Variables** tab
4. Locate the constant: **showRecentSRsByPrimaryContact**
5. Update the value based on your requirement:
• Set to **true** to display only Service Requests where the contact is the **Primary Contact** (optimized performance)
• Set to **false** to display all associated Service Requests (primary and secondary contacts)
6. Save and publish your changes

## 💡 Tips and Considerations

n/a

## 🔐 Access Requirements

• Oracle Visual Builder Studio for Application Extension

## 📚 Key Resources

n/a

---
*Oracle Cloud Readiness · 26C · SERVICE · Service Center*