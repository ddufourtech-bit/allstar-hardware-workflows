# Standard LEGO Build Procedure

**Status:** Active Standard  
**Date:** May 2025  
**Author:** Allstar Microelectronics Hardware Technician  
**Platform:** LEGO-style open-frame test chassis (Allstar modular server/workstation benches)

## Overview
This document outlines the standardized LEGO build process used at Allstar Microelectronics. LEGO builds are open-frame test systems used for validation before final shipment. They follow a modular top/bottom chassis design and emphasize thorough Memtest validation and careful component handling.

## Build Process

### 1. Chassis Preparation
- Gather tops and bottoms.
- **Tops:** Attach chassis fans + SSD quick-release clips. Add white bar for add-on card stability.
- **Bottoms:** Attach legs, rubber mounting pads, and motherboard bolts.
- For smaller boards (mATX and below): No top is used — instead mount PSU brackets on the bottom right side.

### 2. Motherboard Preparation
- Retrieve Sales Order & Build list (acts as the build recipe).
- Unbox motherboards and lay them out.
- Attach mounting brackets + heatsink hardware (if design requires).
- Install CPUs → RAM → SSDs (ensure correct slot type: SATA vs NVMe).
- Apply thermal paste → attach heatsinks (handle sharp/delicate heatsinks with care).
- Connect fan cables to header pins.

### 3. Installation & Testing
- Place the populated motherboard into the LEGO chassis.
- Move system to KVM stations.
- Unbox and prep PSUs.
- Connect standard power: 24-pin + two CPU power cables (add PCIe power only if needed for add-on cards; SATA cables only if SSDs/HDDs are part of the build).
- Run Memtest86+ for 72 hours (focused on CPU + RAM stability).

### 4. Shipment / Serials
- After testing, remove systems from KVM.
- Place completed systems on tables in groups of 10.
- Assign serial numbers.
- Label both the LEGO chassis and the shipping box.

### 5. BIOS / IPMI Configuration
- No baseline configuration is applied unless the BIOS version is outdated.
- BIOS is intentionally left at stock version so labs can benchmark consistently.

## Common Quirks & Gotchas

- **CPU installation:** Very easy to bend socket pins — always unbox CPUs as needed, unlatch socket cover, place CPU flat, and align arrows.
- **SSD installation:** Must use correct slot type. Proximity to CPU is important on some boards.
- **Fan headers (especially water-cooled systems):**
  - Chassis fans plug into normal chassis fan headers.
  - Water pumps plug into AIO / CPU fan header pins.
  - RGB lighting requires separate RGB header connections.
- **Memtest failures:** Usually caused by RAM or CPU issues. Temperature warnings on CPUs and SSDs are also common.
- **PSU setup:** Minimal cabling (24-pin + two 8-pin CPU) unless add-on cards or drives require extra power.

## Lessons Learned
- Always follow the Sales Order/Build list exactly — it is the definitive recipe.
- Thorough 72-hour Memtest catches the majority of CPU/RAM issues before shipment.
- Proper handling of delicate heatsinks and careful CPU socket alignment prevents bricked components.
- Fan and pump header placement must be verified on every water-cooled LEGO build.

**Status:** This procedure was the current working standard for all LEGO builds during tenure.  
**Last Updated:** 5/16/2026