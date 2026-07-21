[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Human Resources](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/human-resources.md)

# Override Display Properties for Programmatically Shown Redwood Employment Process Sections

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hure-26c/26C-hr-wn-f49408.htm)

Display properties for Redwood Employment Processes can now be overridden for sections that are shown programmatically, such as Contracts. The following table lists the page properties that can be configured, along with their classifications, labels, descriptions, and availability in Local and Global Transfer and Change Worker Type.

Page Property | Classification | Label | Description | Available in Local and Global Transfer | Available in Change Worker Type
hidePersonNamehidePersonName | Names | Hide Person Name Section | Controls the display of the Person Name section. Set it to Yes to hide the section. Default value is to show the section. | Yes | NA
hideBiographicalInformation | Biographical info | Hide Biographical Information Section | Controls the display of the Biographical Information section. Set it to Yes to hide the section. Default value is to show the section. | Yes | NA
hideNationalIdentifier | National Identifier | Hide National Identifier Section | Controls the display of the National Identifier section. Set it to Yes to hide the section. Default value is to show the section. | Yes | NA
hidePersonLegislativeInfo | Legislative info | Hide Person Legislative Info Section | Controls the display of the Person Legislative Info (Demographics) section. Set it to Yes to hide the section. Default value is to show the section. | Yes | NA
hideContractInfo | Contract info | Hide Contract Info Section | Controls the display of the Contract Info section. Set it to Yes to hide the section. Default value is to show the section. | Yes | Yes
hideImpactedAssignments | Impacted assignments | Hide Impacted Assignments Section | Controls the display of the Impacted Assignments section. Set it to Yes to hide the section. Default value is to show the section. | Yes | Yes

The enhancement gives greater control over Redwood Employment Processes and helps manage section visibility in line with business needs.

## ⚙️ Steps to Enable and Configure

You need to set the *above*page properties to an appropriate value to change the default behavior.

## 📚 Key Resources

For more information refer to these resources on the Oracle Help Center:

• Employment Processes in the Using Global Human Resources guide
• Extending Redwood Applications for HCM and SCM Using Visual Builder Studio guide

---
*Oracle Cloud Readiness · 26C · HCM · Human Resources*