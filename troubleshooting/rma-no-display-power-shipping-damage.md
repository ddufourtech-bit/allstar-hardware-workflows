# RMA: No Display / Power Issues – Shipping Damage

**Status:** Resolved (Motherboard RMA'd)  
**Date Received:** 2025-06-30  
**Chassis:** Standard LEGO Server  
**Motherboard:** Supermicro H12DSi-N6  

## Problem Summary
System arrived with visible physical damage. Powered on with Power LED lit but no display output and no IPMI access.

## Troubleshooting Performed
1. Inspected packaging: Shipped upside down, no protection bar, no chassis fans, non-anti-static materials contacting motherboard.
2. Documented physical damage: serial port damage, chipping on motherboard edge near PCIe slots, DisplayPort connector bent inward.
3. Attempted bypass with add-in video card — no change.
4. Powered system: Power LED on, no POST, no IPMI.
5. Decision: RMA motherboard due to physical damage.

## Root Cause
Physical shipping damage from improper packaging and orientation.

## Resolution
Motherboard RMA'd to Supermicro on 2025-07-02. Remaining components scheduled for testing on known-good board.

## Lessons Learned
- Photograph and document all incoming shipping damage immediately.
- Non-anti-static packing materials can cause contact shorts or ESD.
- Bent connectors + chipped PCB edges are strong indicators of board-level failure.
- Test with alternate display output before declaring display failure.

**Status:** Closed  
**Last Updated:** May 16, 2026
