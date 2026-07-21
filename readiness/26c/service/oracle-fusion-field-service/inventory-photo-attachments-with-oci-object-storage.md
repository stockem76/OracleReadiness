[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Oracle Fusion Field Service](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/oracle-fusion-field-service.md)

# Inventory Photo Attachments with OCI Object Storage

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/fscv-26c/26C-fsvc-wn-f49614.htm)

Starting from 26C, Inventory Photo Attachments feature allows field resources to take and attach multiple photos directly to Inventory or Inventory Forms while working in the field. The photos are automatically uploaded to OCI Object Storage, making them available for customer record systems, compliance tracking, and asset documentation workflows.

The Inventory Photo Attachments feature allows field resources to take and attach multiple photos directly to Inventory or Inventory Forms while working in the field. The photos are automatically uploaded to OCI Object Storage, making them available for customer record systems, compliance tracking, and asset documentation workflows.

Field resources can:

• Capture multiple photos for a single inventory item
• Add photos to a form while adding or editing inventory
• Crop or annotate images before saving
• Preview and review captured images
• Continue working offline, with photos syncing automatically when connectivity returns

**Supported Use Cases**

The feature is intended for serialized inventory and asset management scenarios where visual proof or condition tracking is important. Examples include:

• Utility equipment inspections
• Construction asset verification
• Parts installation confirmation
• Damage documentation
• Inventory audits
• Migration scenarios from Oracle Field Service to Fusion Field Service

**Integration**

OCI Object Storage serves as an intermediate storage location for photos captured in the field. In most implementations, customers or partners transfer these images to their own system of record for long-term storage, asset management, or business processing.

The integration flow typically consists of two stages:

• Identifying the required photos in OCI Object Storage
• Transferring the photos to the customer’s target system and associating them with the appropriate business object or asset record

**Photo File Name Pattern**

Photos captured from Field Service are automatically named using a structured naming convention to simplify identification and downstream processing.

`({Timestamp}_{Work_Order}_2_{Inventory_Id}_{Property_Label})`

  Where:

• Timestamp — Date and time the photo was captured, in yyyy/mm/dd hh:mm:ss format
• Work_Order — Work order number associated with the inventory item
• 2 — Inventory entity identifier in Field Service
• Inventory_ID — Identifier of the inventory item associated with the photo
• Property_Label — Label of the Attachments property used to capture the image

**Object Storage Folder Structure**

Objects are organized using the following folder naming pattern:

`2_{Inventory_Id}_{Work_Order}_{Property_Label}`

Where:

• 2 — Inventory entity identifier in Field Service
• Inventory_ID — Identifier of the inventory item
• Work_Order — Associated work order number

This structure enables integrators to efficiently locate and process files related to a specific inventory item or work order.

## 🎯 Business Benefit

• Enables asset-based management scenarios by allowing field resources to capture and associate photos directly with inventory and assets.
• Improves field documentation for industries such as utilities and construction, where visual asset verification is critical.
• Improves traceability and auditability of installed or serviced inventory items.
• Supports offline field operations by caching photos locally and synchronizing them automatically when connectivity is restored.
• Reduces migration complexity for customers transitioning to Fusion Field Service by providing functionality aligned with common Field Service attachment workflows.

## ⚙️ Steps to Enable and Configure

The feature is enabled through application configuration. To configure Inventory Photo Attachments:

1. Create an application for OCI Object Storage.
2. Create an **Attachments**property.
3. Select the **Inventory** entity.
4. Associate the property with the OCI Object Storage application.
5. Add an Inventory Attachments property to an Inventory form.
6. Add a button to the Add/Edit Inventory screen configured to launch the Inventory form.

## 💡 Tips and Considerations

N/A

## 📚 Key Resources

• **Capturing Geolocation and Watermark**

   The Multi-Image Watermark feature is fully supported for Inventory Photo Attachments, enabling watermarking capabilities for photos captured and attached to inventory items.
• **Searching for Photos**

   Integrators can use the Searching for Object Storage in a Bucket functionality to locate the required files within OCI Object Storage.
• **Downloading Photos to the Target System**

   After identifying the required images, integrators can use the Object Storage Object from a Bucket API to download photos from OCI Object Storage and transfer them to downstream applications or enterprise systems.

---
*Oracle Cloud Readiness · 26C · SERVICE · Oracle Fusion Field Service*