[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# REST Enabled Action - Change Service Provider

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f46517.htm)

This feature extends the existing Change Service Provider functionality by making it available through a REST-enabled Shipment Business Action. You can now programmatically retrieve and evaluate alternative service provider options for shipments using an API-based workflow.  The REST-enabled Business Action allow you to incorporate the action-based functionality into your AI Agents, and other automated business processes.

This Change Service Provider REST-enabled Shipment Business Action allows you to programmatically retrieve and evaluate alternative service provider options for shipments,

**Request Input:**

"pks": {

                          "description": "Array of shipment PKs when not using path id.",

                          "type": "array",

                          "items": {

                              "type": "string"

                          }

                      },

                      "relaxEquipment": {

                          "description": "If not provided, the value will depend on the property glog.webserver.shipment.changeSP.ignoreEquipment.",

                          "type": "string"

                      },

                      "relaxMode": {

                          "description": "If not provided, the value will depend on the property glog.webserver.shipment.changeSP.ignoreMode.",

                          "type": "string"

                      },

                      "relaxServiceTime": {

                          "description": "If not provided, the value will depend on the property glog.webserver.shipment.changeSP.ignoreServiceTime.",

                          "type": "string"

                      },

                      "ratePreference": {

                          "description": "If not provided, the value will depend on the property glog.webserver.shipment.changeSP.showpreferredOnly.",

                          "type": "string"

                      },

                      "showDigitalFreightRates": {

                          "description": "If not provided, the value will depend on the property glog.webserver.shipment.changeSP.showDigitalFreightRates.",

                          "type": "string"

                      }

**Input Example:**

{

  "relaxEquipment": "false",

  "relaxMode": "false",

  "relaxServiceTime": "false",

  "showDigitalFreightRates": "false",

  "ratePreference": "2",

  "pks":[

  "SHIP.67375","SHIP.67395"

  ]

  }

**Response:**

"description": "Service provider option for the shipment",

                  "type": "object",

                  "properties": {

                      "serviceProviderId": {

                          "description": "Service Provider Id",

                          "type": "string"

                      },

                      "transportModeGid": {

                          "description": "Transport Mode Gid",

                          "type": "string"

                      },

                      "rateOfferingGid": {

                          "description": "Rate Offering Gid",

                          "type": "string"

                      },

                      "rateGeoGid": {

                          "description": "Rate Geo Gid",

                          "type": "string"

                      },

                      "equipmentGroupGid": {

                          "description": "Equipment Group Gid",

                          "type": "string"

                      },

                      "sourceLocationGid": {

                          "description": "Source Location Gid",

                          "type": "string"

                      },

                      "destinationLocationGid": {

                          "description": "Destination Location Gid",

                          "type": "string"

                      },

                      "isServiceTimeFeasible": {

                          "description": "Indicates whether the service time is feasible.",

                          "type": "string"

                      },

                      "isServProvPreferred": {

                          "description": "Indicates whether the preferred service provider selected.",

                          "type": "string"

                      },

                      "isDigitalFreight": {

                          "description": "Indicates whether this service provider is a digital freight provider.",

                          "type": "string"

                      },

                      "tenderStatus": {

                          "description": "Indicates current tender status",

                          "type": "string"

                      },

                      "totalCost": {

                          "description": "Total Cost",

                          "allOf": [

                              {

                                  "$ref": "#/components/schemas/currencyType"

                              }

                          ]

                      },

                      "totalWeightedCost": {

                          "description": "Total Weighted Cost",

                          "allOf": [

                              {

                                  "$ref": "#/components/schemas/currencyType"

                              }

                          ]

                      },

                      "startTime": {

                          "description": "Start Time",

                          "allOf": [

                              {

                                  "$ref": "#/components/schemas/dateTimeType"

                              }

                          ]

                      },

                      "endTime": {

                          "description": "End Time",

                          "allOf": [

                              {

                                  "$ref": "#/components/schemas/dateTimeType"

                              }

                          ]

                      },

                      "commitmentAllocation": {

                          "description": "Commitment Allocation Details",

                          "allOf": [

                              {

                                  "$ref": "#/components/schemas/commitmentAllocationType"

                              }

                          ]

                      },

                      "commitmentCount": {

                          "description": "Commitment Count Details",

                          "allOf": [

                              {

                                  "$ref": "#/components/schemas/commitmentCountType"

                              }

                          ]

                      },

                      "capacityUsage": {

                          "description": "Capacity Usage Details",

                          "allOf": [

                              {

                                  "$ref": "#/components/schemas/capacityUsageType"

                              }

                          ]

                      },

                      "co2Emission": {

                          "description": "CO2 Emissions Details",

                          "allOf": [

                              {

                                  "$ref": "#/components/schemas/weightType"

                              }

                          ]

                      },

                      "co2EqEmission": {

                          "description": "CO2 Equivalent Emissions Details",

                          "allOf": [

                              {

                                  "$ref": "#/components/schemas/weightType"

                              }

                          ]

                      }

"shipmentPk": {

                          "description": "Pk of the shipment",

                          "type": "string"

                      },

                      "firstOrderReleaseGid": {

                          "description": "First Order Release GID",

                          "type": "string"

                      }

**Business Benefit:** This feature allows you to programmatically retrieve and evaluate alternative service provider options for shipments using an API-based workflow, this allows AI Agents and other automated business processes to interact directly with Change Service Provider capabilities.

## ⚙️ Steps to Enable and Configure

1. Confirm that your integration users have access to the shipment business actions and REST services required for shipment updates and service provider evaluation.
2. Identify the shipment records that require service provider evaluation or reassignment.
3. Invoke the REST-enabled Change Service Provider business action using the shipment primary keys as input.
4. Optionally configure evaluation behavior using the available request parameters: 
  • Relax equipment matching requirements
• Relax transportation mode matching requirements
• Relax service time feasibility requirements
• Restrict results to preferred service providers
• Include or exclude digital freight providers
5. Review the returned service provider options, including: 
  • Total and weighted transportation costs
• Service feasibility
• Current tender status
• Commitment allocation and commitment count details
• Equipment and transportation mode compatibility
• CO2 and CO2 equivalent emissions data
6. Use the returned service provider information to drive your operational workflow, automated decisioning process, or downstream shipment reassignment actions.

No additional user interface setup is required if you already use REST integrations and shipment business actions.

## 💡 Tips and Considerations

• The service can evaluate multiple shipments in a single request by providing an array of shipment identifiers.
• If you do not explicitly provide the relaxation parameters, the system uses the existing property settings configured for shipment service provider changes.
• Service provider results may include: 
  • Preferred providers
• Current assigned providers
• Digital freight providers
• Providers that do not fully satisfy service constraints, depending on your parameter selections
• Use the service time feasibility indicator carefully when evaluating lower-cost alternatives. Some providers may not meet the requested timing requirements if service time relaxation is enabled.
• Commitment allocation and commitment count information can help you balance carrier commitments and procurement objectives during reassignment decisions.
• Emissions data is returned with the provider options, allowing you to incorporate sustainability metrics into carrier selection workflows.
• Tender status values help identify whether a provider is currently available or already associated with the shipment.
• The returned results are informational and intended to support service provider evaluation and workflow automation. Your organization should define the business rules that determine how replacement decisions are finalized.

## 📚 Key Resources

The complete REST documentation REST API for Fusion Cloud Transportation and Global Trade Management Business Object Resources can be found here:

https://docs.oracle.com/en/cloud/saas/transportation/26b/otmra/index.html

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*