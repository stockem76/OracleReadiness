[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Transportation Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/transportation-management.md)

# Transportation Operational Intelligence (TOI) Event Lat/Long

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/otm26c/26C-otm-wn-f49361.htm)

This feature extends the Transportation Operational  Intelligence (TOI) Shipment Tracking Event Dimension folder to include Event Latitude and Event Longitude data.  By exposing tracking event latitude and longitude coordinates directly in the reporting structure, you can more easily support map-based visualizations, geographic trend analysis, and location-aware operational reporting.

Event Latitude and Longitude Fields

**Business Benefit:** This feature helps you improve shipment visibility and geographic reporting by making location coordinate data readily available within shipment tracking analytics.

Key benefits include:

1. Reduced manual effort when building location-based reports
2. Improved operational visibility through geographic analysis
3. Easier integration with mapping and visualization tools
4. Better support for route monitoring and shipment event tracking

## ⚙️ Steps to Enable and Configure

1. Navigate to the TOI reporting or analytics area where Shipment Tracking Event Dimensions are available.
2. Open the Shipment Tracking Event Dimensions folder within your reporting subject area.
3. Locate the new fields: 
  • **Event Latitude**
• **Event Longitude**
4. Add these fields to existing or new reports, dashboards, or analytics views as needed.
5. Use the fields for: 
  • Geographic filtering
• Map visualizations
• Regional shipment analysis
• Location-based operational reporting

## 💡 Tips and Considerations

• Latitude and Longitude values are only available when geographic coordinate data exists for the shipment tracking event.
• Reports or dashboards using mapping visualizations may require compatible analytics or third-party visualization tools.
• Consider combining coordinate fields with shipment status, event timestamps, carrier, or location dimensions for more meaningful operational insights.
• Geographic precision depends on the quality and availability of the underlying shipment event data.
• Existing reports are not automatically updated to include the new fields. You must manually add them to custom analytics or dashboards.

---
*Oracle Cloud Readiness · 26C · SCM · Transportation Management*