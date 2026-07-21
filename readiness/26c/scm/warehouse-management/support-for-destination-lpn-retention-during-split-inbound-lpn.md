[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Support for Destination LPN Retention during Split Inbound LPN

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50170.htm)

Mobile Split Inbound Container now provides an option to retain the destination (To) LPN when processing multiple source containers in **Confirm Before SKU Scan** mode. This reduces repeated scanning when users split inventory into the same destination LPN.

When **to-lpn-confirmation-mode** is set to **Confirm before Sku Scan** and users end the From LPN, WMS now clears only the From LPN and keeps the **To LPN**, so users can continue splitting into the same destination LPN. You can clear the To LPN with CTRL-T: End To LPN.

## ⚙️ Steps to Enable and Configure

1. Go to Split IBLPN screen parameters.
2. Set **to-lpn-confirmation-mode** to Confirm before Sku Scan to end the From LPN when changing source LPNs.
3. Use CTRL-T when to clear the To LPN.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*