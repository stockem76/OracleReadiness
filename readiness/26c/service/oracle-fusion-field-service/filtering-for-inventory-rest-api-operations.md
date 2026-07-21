[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SERVICE](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/index.md) › [Oracle Fusion Field Service](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/service/oracle-fusion-field-service.md)

# Filtering for Inventory REST API Operations

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/service/26c/fscv-26c/26C-fsvc-wn-f49545.htm)

Supported inventory-related REST API operations now include a *filter* query parameter that helps integrations retrieve only the inventory records that match specific conditions. Previously, integrations had to retrieve all inventory records for an activity or resource and then filter the response in the client code.

With Update 26C, integrations can include a filter expression in the API request. The response includes only the inventory records that match the filter, which can reduce response size and simplify integration logic. For example, an integration that checks whether a technician has a required modem or cable box can request only inventory records for that inventory type instead of retrieving the technician’s full inventory list.

The *filter* query parameter is available for these inventory-related REST API operations:

• Get Customer Inventories
• Get Installed Inventories
• Get Deinstalled Inventories
• Get Resource Inventories

As part of this update:

• The supported inventory-related REST API operations now include a *filter* query parameter.
• Filter expressions can include the  *inventoryType*, *serialNumber*, and *quantity* inventory fields.
• The *inventoryType*, *serialNumber*, and *quantity* fields can be filtered by using equal to (==) and not equal to (!=).
• The *quantity* field can also be filtered by using less than (<), greater than (>), less than or equal to (<=), and greater than or equal to (>=).
• Multiple filter conditions can be combined with supported logical operators AND, OR, and NOT.
• Filtering is applied before pagination, so returned items and totals are based on the filtered results.

**Filter Syntax and Examples**

A filter expression must evaluate to a boolean value. The expression can include one or more comparison statements joined by supported logical operators.

Use this format:

  <field> <operator> <literal>

**Supported Fields**

Field | Data Type
inventoryType | String
serialNumber | String
quantity | Number

String values must be enclosed in single quotes. Numeric values must not be enclosed in quotes.

**Valid Examples**

?filter=quantity>10 AND inventoryType=='CABLEBOX'

?filter=serialNumber=='ABC123'

?filter=inventoryType!='UNITS'

?filter=quantity<10 AND serialNumber=='ABC123' AND inventoryType=='MODEM'

**Rules Applicable to Filter Expressions**

These rules apply to filter expressions:

• The expression must evaluate to a boolean value.
• The expression may contain one or more comparison statements.
• Multiple comparison statements can be combined using logical operators (AND, OR, NOT).
• Only supported fields may be used.
• String fields support only == and !=.
• Numeric comparisons are supported only for quantity.

**Validation and Error Handling**

The API validates the filter expression before returning inventory records. If the filter expression is not valid, the API returns 400 Bad Request.

The API returns 400 Bad Request when the filter contains:

• Invalid filter syntax
• Unsupported operators
• Invalid data types
• Malformed string literals
• Unsupported fields

For example, the following filter is not valid because quantity requires a numeric value without quotes:

?filter=quantity=='1'

The following filter is not valid because numeric comparison operators are not supported for string fields such as inventoryType:

?filter=inventoryType>=2

The following filter is not valid because serialNumber1 is not a supported filter field:

?filter=serialNumber1=='provider'

The response identifies the unsupported field:

{
"type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10.4.1",
"title": "Bad Request",
"status": "400",
"detail": "Unsupported filter field: serialNumber1"
}

The following filter is not valid because less than or equal to is not supported for serialNumber:

?filter=serialNumber<='qwerty'

The response identifies the unsupported operator for the field:

{
"type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10.4.1",
"title": "Bad Request",
"status": "400",
"detail": "Invalid filter operator for field 'serialNumber'"
}

**Processing Logic**

  Filter expressions are processed before the API response is returned:

• The filter expression is parsed and validated.
• Supported filter conditions are applied to the inventory records.
• Filtering is applied before pagination.
• The response includes only the inventory records that match the filter.

## 🎯 Business Benefit

• Reduces the amount of inventory data returned by REST API calls.
• Improves API performance and efficiency.
• Eliminates additional client-side filtering logic in integrations.
• Simplifies integration code for customers who need to find specific inventory items.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

---
*Oracle Cloud Readiness · 26C · SERVICE · Oracle Fusion Field Service*