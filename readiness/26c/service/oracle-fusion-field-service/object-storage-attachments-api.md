[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Oracle Fusion Field Service](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/oracle-fusion-field-service.md)

# Object Storage Attachments API

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/fscv-26c/26C-fsvc-wn-f49514.htm)

The Object Storage Attachments API enables organizations to associate files stored securely in Oracle Cloud Infrastructure (OCI) Object Storage with operational data in Oracle Fusion Field Service.

Using this capability, organizations can manage documents, images, and other files in OCI Object Storage, while allowing Oracle Fusion Field Service users to access related file information for activities and inventory records.

The API allows to manage just file metadata references such as 'fileName' and 'URI' . It doesn't check if a file defined in the request is present in OCI Object Storage.

This feature can be used in scenarios such as:

• Linking externally stored work order documents, manuals, or compliance certificates to field activities
• Associating photos, inspection images, or proof-of-service files with service operations
• Managing inventory-related documents, such as warranty records or asset images
• Supporting integrations where external enterprise systems manage file storage while Oracle Fusion Field Service maintains operational references to those files

The feature currently supports file associations for the following Oracle Fusion Field Service business entities:

• Activities
• Inventories

**API Description**

URL path:

• Activities: 
  • GET  /api/field-service/core/v1/activities/{activityId}/externalFilesInfo/{propertyLabel}
• PUT  /api/field-service/core/v1/activities/{activityId}/externalFilesInfo/{propertyLabel}
• Inventory: 
  • GET  /api/field-service/core/v1/inventories/{inventoryId}/externalFilesInfo/{propertyLabel}
• PUT  /api/field-service/core/v1/inventories/{inventoryId}/externalFilesInfo/{propertyLabel}

**Authentication and Authorization**

The Object Storage Attachments API supports the same authentication and authorization methods available for other Oracle Fusion Field Service REST APIs, including Basic Authentication, OAuth token-based authentication, and other supported platform authorization mechanisms.

**Example Request**

   1. GET

curl --url "https://custname.fs.ocs.oraclecorp.com/api/field-service/core/v1/activities/
{activityId}/externalFilesInfo/{propertyLabel}" 
\     -H "Authorization: ***" \      --get \

**Example of GET Response**

{
  "items": [
    {
      "fileName": "spec.pdf",
      "contentType": "application/pdf",
      "fileSize": 12345,
      "URI": "oci://bucket/path/spec.pdf"
    }
  ]
}

**Field Definitions**

This table provides the definitions of the fields used in the API.

Field Name | Description | Remarks
fileName | Display name | Recommended to match the last segment of the URI, but not required.
contentType | MIME type | Used for downstream user experience and rendering decisions.
fileSize | Size in bytes | If omitted, the service applies a best-effort default value.
URI | OCI object reference | Used as the unique identifier during update and merge operations.

2. PUT

curl --url 'https://custname.fs.ocs.oc-test.com/api/field-service/core/v1/activities/
{activityId}/externalFilesInfo/{activityId}' 
\
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer <your_token>'-d  ' {
"operationType" : "update",
"items": [
{
"fileName": "samplefilename.jpg",
"contentType": "image/jpeg",
"fileSize": 11,
"URI": "sample_path/samplefilename.jpg"
}
]
}'

**Example of PUT Response**

204 No content

If "operationType" is not specified in the request body, the default value is "replace".

**Operation Semantics**
**replace (default)**

  The "replace" operation updates the linked file list to match the request exactly. Here's how it works:

• Files not included in the request are removed from the existing list.
• Removed files are soft-deleted in the backend representation.
• If items: [ ] is provided, all linked files are cleared for the specified entity.

**update (merge / upsert)**

  The "update" operation adds or updates files without replacing the existing list. Here's how it works:

• Files are matched using the URI field.
• If URI exists, the API updates the metadata for that file.
• If URI doesn't exist, the API adds the file as a new entry.
• Files not included in the request remain unchanged.

## 🎯 Business Benefit

• Supports business processes requiring access to manuals, compliance documents, inspection records, or proof-of-service files
• Enables mobile workers to access externally stored files directly from their Oracle Fusion Field Service activities
• Supports centralized and scalable file storage using OCI Object Storage
• Allows organizations to manage attachment metadata through standard REST APIs for easier automation and system integration

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

**Prerequisites**

• The target propertyLabel must be configured for the applicable entity type and available through lookup configuration.
• The calling application must have required OAuth scopes: 
  • platform:core_api_activity:read | write 
    • GET operations require read permissions for Activity entities
• PUT operations require write permissions for Activity entities
• platform:core_api_inventory:read | write 
    • GET operations require read permissions for Inventory entities
• PUT operations require write permissions for Inventory entities
• The referenced OCI Object Storage files must exist. The API stores and manages metadata references only.

---
*Oracle Cloud Readiness · 26C · SERVICE · Oracle Fusion Field Service*