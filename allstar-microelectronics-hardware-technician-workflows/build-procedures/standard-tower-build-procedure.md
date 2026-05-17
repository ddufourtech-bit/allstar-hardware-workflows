# Standard Tower Build Procedure

**Status:** Active Standard  
**Date:** May 2025  
**Author:** Allstar Microelectronics Hardware Technician  
**Platform:** High-end tower chassis (consumer and workstation towers)

## Overview
This document outlines the standardized tower build process used at Allstar Microelectronics. Tower builds follow the same core motherboard preparation as server builds but include tower-specific considerations for chassis layout, built-in front-panel controls, cable routing, and final testing/shipment preparation.

## Build Process

### 1. Chassis Preparation
- Carefully unbox the chassis to avoid damaging Styrofoam or side panels.
- Install motherboard mounting bolts in the correct locations (form factor dependent).
- Install the I/O shield.
- Add any extra chassis fans as required by the build specification.

### 2. Motherboard Preparation
- Follow the standard server build motherboard preparation steps:
  - CPU installation
  - RAM population (following slot rules and motherboard manual)
  - Heatsink / cooler installation
- **Tower-specific note:** Towers have built-in power/reset/HDD LED/power LED buttons and lights (no separate power block required like some open-air test benches).

### 3. Motherboard Installation
- Attach the USB 3.0 cable to the motherboard **before** mounting the board (limited space and awkward angle after installation increases risk of bending pins).
- Only pre-attach the USB 3.0 cable — other cables are easier to reach after the motherboard is mounted.
- Mount the motherboard securely into the chassis.

### 4. PSU Installation
- If the PSU is bottom-mounted, install it upside down for improved airflow.
- Plug in **all** necessary PSU cables **before** mounting the PSU (space and depth make post-installation connections difficult).

### 5. Cable Installation
- Start with smaller, low-profile cables:
  - HD Audio
  - USB
  - Chassis fans
- Then install the main power cables:
  - 24-pin main power
  - Two 8-pin CPU power cables
  - PCIe power cables (for GPUs)
  - SATA power (if applicable)
- Ensure correct orientation so cables lay flat and do not twist or take up unnecessary space.
- Install power and LED cables **last** (they are small and more prone to coming loose).
- Pay close attention to the motherboard power pinout and positive/negative orientation for front-panel connectors.

### 6. Cable Management
- Prioritize flat runs and a tidy, professional layout (both visual and functional).
- Use Velcro straps and existing chassis channels for clean, serviceable routing.

### 7. Testing
- Move the tower to the KVM station.
- Power on and check for LED warning lights, beep codes, and sensor readings.
- If clear, enter BIOS:
  - Update time/date (required for every system based on final destination).
  - Flash BIOS if needed.
- Run Memtest.
- If required by the build: install OS and test full system functionality.

### 8. Shipment Preparation
- Once all tests pass, prepare the system for shipping.

## Lessons Learned
- Pre-attaching the USB 3.0 cable before motherboard installation prevents pin damage.
- Installing PSU cables before mounting the PSU avoids major access issues in tight tower layouts.
- Proper sequencing (small cables first, power cables next, front-panel last) reduces rework during cable management.
- Always verify BIOS time/date and run Memtest on every tower before shipment.

**Status:** This procedure was the current working standard for all tower builds during tenure.  
**Last Updated:** 5/16/2026