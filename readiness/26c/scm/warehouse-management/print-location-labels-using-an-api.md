[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Print Location Labels using an API

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f49716.htm)

The Print Location Labels API will determine the label template if rules are configured for this label type in the Label Rules Engine UI. The label_designer_code will be optional as part of the API parameters.

**GET API URL**

The GET API will return the ZPL representation of the label.

`<BASE_URL>/wms/lgfapi/v10/print/label/location/?barcode=LOC001`

**More GET Examples**

`GET: BASE_URL/wms/lgfapi/v10/print/label/location/?barcode=LOC001`

`GET: BASE_URL/wms/lgfapi/v10/print/label/location/?barcode__in=LOC001,LOC002`

`GET: BASE_URL/wms/lgfapi/v10/print/label/location/facility_id__code=FAC1&id__in=101,102,103&labe`

**SAMPLE RESPONSE**

{

    "record_count": 2,

    "success_count": 2,

    "failure_count": 0,

    "data": {

        "LOC001": "Cl5YQQpeTEgwLDBeTFJOCl5DSTI4CgpeQ1d...",

        "LOC002": "Cl5YQQpeTEgwLDBeTFJOCl5DSTI4CgpeQ1dULF5G..."

    },

    "details": null

}

**POST API URL**

The POST API will submit the label for printing.

`.../wms/lgfapi/v10/print/label/location`

**SAMPLE RESPONSE**

{

     "parameters":

     {

          "facility_id__code": "FAC1",

          "code": "LOC001"

     },

     "options": {

          "label_designer_code": "location_label_1",

          "printer_name": "PRINTER1",

          "label_count": 1

     }

}

## ⚙️ Steps to Enable and Configure

Review the REST service definition in the REST API guides to leverage (available from the Oracle Help Center > *your apps service area of interest* > APIs & Schema). If you are new to Oracle's REST services you may want to begin with the Quick Start section.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*