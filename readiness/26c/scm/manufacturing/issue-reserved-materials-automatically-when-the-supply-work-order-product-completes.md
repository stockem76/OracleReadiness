[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Manufacturing](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/manufacturing.md)

# Issue Reserved Materials Automatically When the Supply Work Order Product Completes

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/mfg26c/26C-mfg-wn-f44540.htm)

For multi-stage production processes, it is common to model separate, linked work orders to coordinate and track the material flow across stages. For example, the primary output from one stage is accurately supplied as an input to the next stage. These work orders require tight synchronization when managing timing and quantity variations. A reservation created between the work orders ensures that the materials are used exclusively between these stages.

You can now automatically issue reserved materials from a supply work order when the primary product is completed. This automation streamlines the management and execution of related work orders for discrete and process manufacturing based on the physical production process. For discrete work orders the work order product is issued upon completion at the last operation. For process work orders, primary output with a completion type of Automatic is supported.

When a prior reservation exists between a supply work order product and a demand work order operation material, the completed product is automatically issued to the demand work order if both the following conditions are met:

• The material supply type is Push.
• The completion subinventory specified on the supply work order matches the supply subinventory specified for the material on the demand work order.

Upon product completion, the system automatically issues the material to the demand work order and relieves the reservation.

Work Order Material Manual Reservation

Work Order Product Reserved to Work Order Operation Material

Reserved Material Auto Issued upon Product Completion

**Changes to REST**:

The auto issue of reserved materials is supported when the work order product is completed using the operationTransactions REST service for both discrete and process work orders.

**Changes to FBDI**:

The auto issue of reserved materials is supported when the work order product is completed using the WorkOrderOperationTransaction FBDI for discrete and ProcessWorkOrderOperationTransaction FBDI for process, and the ADFdi corrections spreadsheet.

This feature provides the following benefits:

• Automates component usage updates, reducing user workload and transaction volume.
• Improves material accuracy and traceability.
• Ensures component consumption scales correctly with actual production.
• Reduces errors and delays from manual material issues.
• Provides smoother execution and reliable costing for work order processing.

*Here's the demo of these capabilities:*

## ⚙️ Steps to Enable and Configure

This feature is enabled for permanent Opt-in.

Feature Available for Opt-In

## 💡 Tips and Considerations

• You can use this feature with discrete or process manufacturing work orders and items with and without lot and serial control.
• For process work orders, primary output with a completion type of Manual is not supported.
• A reservation between the work orders must be created before using this feature.
• It is optional to use work order groups in conjunction with this feature.

## 🔐 Access Requirements

There are no new privileges to use this feature. Users with the existing privileges to perform product completion transactions can access this feature.

## 📚 Key Resources

• Watch the Issue Reserved Materials Automatically When the Supply Work Order Product Completes demo.
• Oracle Fusion Cloud SCM: Refer to the Using Manufacturing guide, available on the Oracle Help Center.
• Oracle Fusion Cloud SCM: Refer to the Implementing Manufacturing and Supply Chain Materials Management guide, available on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Manufacturing*