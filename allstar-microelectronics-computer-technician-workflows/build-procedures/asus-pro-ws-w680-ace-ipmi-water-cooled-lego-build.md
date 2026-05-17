# Build Procedure: ASUS PRO WS W680-ACE IPMI + Water-Cooled LEGO System

**Status:** Completed & Verified  
**Date:** May 2025  
**Motherboard:** ASUS PRO WS W680-ACE IPMI  
**Platform:** High-end AMD system with dedicated remote management  
**Base Procedure:** Follows [Standard LEGO Build Procedure](../standard-lego-build-procedure.md)

## Overview
This build followed the standard LEGO workflow with two major additions:
- Full water cooling loop (pump + radiator)
- ASUS IPMI Expansion Card + GPU installation

## Build Process (LEGO Standard + Specific Additions)

### 1. Motherboard Preparation (Bench)
- Installed CPU, RAM, and M.2 SSD(s) on the ASUS PRO WS W680-ACE IPMI motherboard outside the chassis.
- Applied high-quality thermal paste.

### 2. Chassis & Motherboard Installation
- Prepared LEGO chassis (tops/bottoms, fans, mounting hardware).
- Placed the populated motherboard into the LEGO chassis.

### 3. Water Cooling Pump Installation
- Installed the water block and pump assembly onto the CPU **after** the motherboard was in the chassis.

### 4. Card Installation (GPU + IPMI Expansion Card)
- With the top still removed, installed both the GPU and the ASUS IPMI Expansion Card into their PCIe slots.
- Connected **all** cables from the IPMI card to the motherboard (power, management, fan control, sensor, and USB cables).

### 5. Cable Attachment & Water Cooling Integration
- Attached all power, data, front-panel, and management cables while the top was still off.
- Routed and dressed every cable (especially the large number of IPMI cables) using Velcro straps.
- Connected water pump to the AIO/CPU fan header and verified RGB lighting headers.

### 6. Top Installation
- Secured the top of the LEGO chassis as soon as possible.  
  **Reason:** The top is mechanically linked to the motherboard via the water pump and radiator.

### 7. Final Cable Management & Testing
- Performed final cable management pass.
- Moved system to KVM station.
- Powered on and confirmed successful POST.
- Accessed IPMI/BMC interface via dedicated port and verified remote management features.
- Ran full Memtest86+ (72 hours) and load-tested water pump, fans, GPU, and overall stability.

## Lessons Learned
- The ASUS IPMI card generates a large number of cables — routing them while the top is still off is essential.
- Water pump and radiator integration requires the top to be installed ASAP to avoid stressing tubing.
- Proper fan/pump header placement and RGB connections are critical on water-cooled LEGO systems.

## Evidence
- Bench preparation (CPU/RAM/M.2)
- Motherboard in LEGO chassis
- Water pump installation
- IPMI card + GPU installation (top off)
- Cable dressing and top installation
- Final system with clean management

**Status:** Fully Operational – Remote management and water cooling both functioning reliably.  
**Related Documents:**  
- [Standard LEGO Build Procedure](01-build-procedures/standard-lego-build-procedure.md),(04-evidence/asus-pro-ws-w680-ace-ipmi-water-cooled-lego-build)