[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Warehouse Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/warehouse-management.md)

# Enhancements to Create LPN for Pallet Handling

`⚙️ Steps to Enable`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/logistics/26c/wms26c/26C-wms-wn-f50165.htm)

Warehouses often create Inbound LPNs and place them on pallets during Receiving. Today, users may need separate steps to palletize LPNs, capture pallet details, print labels, confirm locations, or support cross-dock movement.

With this enhancement, users can complete more of this work directly in the Create LPN flow. This helps receiving teams process inventory faster, improve pallet tracking, reduce manual follow-up, and keep inventory tied to the correct pallet and location.

**PALLETIZE LPNS DURING CREATE LPN**

We have enhanced WMS to support pallet handling during Create LPN transaction.  This flow applies to Create LPN and Create LPN from Active.

• The screen parameter **lpn-as-physical-pallet**is now reused as **pallet-handling** with supported values are:
• **Blank**: WMS retains the existing Create LPN flow.
• **LPN as Physical Pallet** : WMS retains existing behaviour of LPN as physical pallet.
• **Palletize up front** : 
• When pallet-handling is set to Palletize up front, WMS prompts users to scan or enter a pallet number before entering the LPN number.
• Users can create multiple LPNs under the same pallet number.
• WMS retains the pallet number until the user ends the pallet.
• A new hot key, **CTRL-E: End Pallet** is introduced that ends the pallet and clears the pallet number.

**CROSS-DOCK SUPPORT FOR PALLETIZED LPNS**

Warehouse operations often require the rapid movement of palletized inventory to fulfill urgent outbound orders without storing inventory in the warehouse. Cross-Dock (Xdock) enables users to route inbound inventory (pallets/LPNs) directly from the **Create LPN** flow to outbound staging areas, bypassing storage locations. In 26C, we have enhanced Xdock support for palletized LPNs through Create LPN to improve inventory handling and streamline shipping operations.

When an LPN is palletized and users end a pallet, WMS allow Xdock operations by checking whether an order has a matching required pallet number and matching inventory.

• If WMS finds a matching order, it Xdocks the inventory to that order.
• If WMS does not find a matching required pallet number, it can create a new order and perform Xdock processing.
• WMS updates the outbound LPN with the correct pallet number.

This applies to Create LPN and Create LPN from Active transactions and this behaviour works with the existing xdock-iblpn setup.

**CAPTURE PALLET IMAGES DURING PALLETIZATION**

WMS now supports pallet image capture during the Create LPN palletization flow. By image capturing feature, users can now capture the Pallet when LPNs are palletized to validate the Pallet's condition.

• New screen parameter: **capture-pallet-image**is introduced with following values: 
• Yes : When the parameter is Yes, users can capture pallet images after selecting CTRL-E: End Pallet.
• No/Blank (default) : When the parameter is No or Blank, WMS keeps the existing flow and does not capture images.
• The captured images are linked to the pallet and users can view the images from the Pallet UI and Pallet Inquiry.

**NOTE****:**Mobile users can capture images, but they cannot attach existing image files.

• Users can capture multiple images for the same pallet and Number of attachments are  incremented based on the images captured. User should be able to click on the link and view images.

**PRINT PALLET LABELS ON END PALLET**

Integrating pallet label printing with Create LPN enables warehouse users to print labels immediately during receiving, improving accuracy, speeding up processing, and enhancing inventory tracking for more efficient warehouse operations. WMS now supports pallet label printing when users end a pallet in Create LPN.

• A new screen parameter: **print-pallet-labels**is introduced with following values:
• No/Blank (Default): WMS does not print a pallet label
• Yes: When the user selects CTRL-E: End Pallet, WMS displays a message - 'label print triggered for pallet% and starts pallet label printing.
• WMS writes label print history in the Label Printing UI. 
• If Label Rules Engine is configured, WMS uses it to print the label.
• If Label Rules Engine is not configured, WMS uses the label template setup.
• Users must have the required printer setup. If no default printer exists, WMS continues to display the existing printer warning “No default printer found, label printing will fail, proceed?”.
• Users can disable the label print initiation message from Facility Message Configuration.

**MANDATORY LOCATION PROMPT CONTROL**

Create LPN streamlines inbound receiving by enabling operators to create and direct inbound LPNs to the appropriate warehouse location during the receiving process. Making the location prompt configurable allows warehouse managers to enforce location capture based on operational requirements, ensuring accurate inventory placement and improved warehouse visibility.

In 26C, we are enforcing location prompt control that helps reduce floor search time, improves inventory traceability, and supports more efficient warehouse operations. WMS now gives facilities more control when users try to complete Create LPN without scanning a required location.

• A new configurable message “Location not Scanned. Proceed” is introduced and facilities can configure the message as Warning, Error, or Disabled. This message displays when you perform CTRL-W and CTRL-X.
• This applies when prompt-location is Yes, and the user tries to complete or exit the transaction without scanning a location.
• If configured as **Error**, the user must scan a valid location before completing the transaction.
• If configured as **Warning**, the user can acknowledge the message and continue.
• If disabled, WMS does not show the message and keeps the existing behaviour.

## ⚙️ Steps to Enable and Configure

**To palletize LPNs, do the following:**

1. Go to the **Create LPN** screen parameters.
2. Set **pallet-handling** based on your receiving process:
• Use **Blank** to keep the current flow.
• Use **LPN as Physical Pallet** for the existing physical pallet behavior.
• Use **Palletize up front** to scan a pallet before creating LPNs.
3. Set **capture-pallet-image** to **Yes** if users need to capture pallet images during CTRL-E: End Pallet.

**To print pallet labels on End Pallet, do the following:**

1. Set **print-pallet-labels** to **Yes** if WMS should print pallet labels when users end a pallet.
2. Confirm that printer setup, Label Rules Engine, or label template setup is complete before enabling pallet label printing.

**To support Palletized Lpns during Cross-Doc, do the following:**

1. Review xdock-iblpn setup if palletized LPNs to support cross-dock processing.
2. Set **prompt-location** to **Yes** if users should scan a location during receiving.
3. Configure the **Location not Scanned. Proceed**. Message as Warning, Error, or Disabled based on your facility process.
4. Use **CTRL-E: End Pallet** after creating all LPNs for a pallet.

---
*Oracle Cloud Readiness · 26C · SCM · Warehouse Management*