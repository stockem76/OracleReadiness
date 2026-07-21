[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Print Item Labels using an API

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f47383.htm)

The Print Item Labels API supports printing item labels for the items associated with an LPN to a specified printer. The API can determine the appropriate label template when item label rules are configured in the Label Rules Engine, and callers can optionally provide a label designer code.

This feature improves automation and reduces manual printing steps by allowing external systems, such as material handling equipment, to request item label printing directly from WMS.

**GET API URL**

The GET API will return the ZPL representation of the label.

`GET.../wms/lgfapi/v10/print/label/item/?label_designer_code=foo`

`GET...//wms/lgfapi/v10/print/label/item?code=ITMCODE&label_designer_code=label_template_ITEM`

**SAMPLE RESPONSE**

{

    "record_count": 2,

    "success_count": 1,

    "failure_count": 1,

    "data": {

        "ITM_1": "VGhpcyBpcyBaUEwgY29kZQ=="

    },

    "details": {

        "ITM_2": "Some error message."

    }

}

**POST API URL**

The POST API will submit the label for printing.

`POST .../wms/lgfapi/v10/print/label/item`

**SAMPLE RESPONSE**

{

    "parameters": {

        "company_id__code": "COM1",

        "barcode": "ITM1"

    },

    "options": {

        "label_designer_code": "label_1",

        "printer_name": "PRINTER1",

        "label_count": 1

    }

}

## ⚙️ Steps to Enable and Configure

Review the REST service definition in the REST API guides to leverage (available from the Oracle Help Center > *your apps service area of interest* > APIs & Schema). If you are new to Oracle's REST services you may want to begin with the Quick Start section.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*