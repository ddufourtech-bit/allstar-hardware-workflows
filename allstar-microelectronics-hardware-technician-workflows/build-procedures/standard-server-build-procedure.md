# Standard Server Build Procedure

**Status:** Active Standard  
**Date:** May 2025  
**Author:** Allstar Microelectronics Hardware Technician  
**Platform:** Supermicro LEGO-style server chassis and similar rackmount/tower servers

## Overview
This document outlines the standardized server build process used at Allstar Microelectronics. It covers chassis preparation, motherboard population, component installation, cabling, and final validation. The procedure ensures consistency, minimizes errors, and produces reliable, client-ready servers.

## Build Process

### 1. Chassis Preparation
- Clear all internal wiring and debris from the chassis.
- Attach motherboard mounting bolts (form factor and chassis dependent).

### 2. Motherboard Preparation
- **CPU Installation**
  - AMD hinged mounting bracket: Slide CPU into rails → press until it clicks → swing bracket down until it clicks → torque cover bracket.
  - Other boards: Use the special plastic CPU installation bracket clipped into the heatsink screw mounts. (Caution: CPU can drop into socket if not secured properly.)
- **Heatsink Installation**
  - Torque screws in a star/cross pattern (similar to mounting a tire).
  - Fans are typically mounted in front of the heatsink, not attached directly to it.

### 3. Fan Headers
- Plug all fans into the appropriate chassis fan header pins on the motherboard.
- **Critical:** CHA_FAN #1 **must** be connected. If left unplugged, the system assumes a fan failure and ramps all other fans to maximum speed (extremely loud).

### 4. RAM Installation
- Populate slots according to the amount of RAM installed.
- ASUS and open-air boards often clearly mark “primary slots.”
- For an odd number of sticks, always refer to the motherboard manual.
- **Note:** Apply these RAM population rules to **all** systems.

### 5. Add-on Cards (Optics, RAID, etc.)
- Most require horizontal installation using PCIe extension/riser cards.
- Secure the card properly:
  - Unscrew the back panel.
  - Place the card.
  - Screw it down securely.
- A loose card can cause RAID failures or system instability.

### 6. RAID / NVMe Cabling
- Run NVMe/data cables from the RAID card to each drive bay.
- Plug power cables into the backplane.
- Manage the chassis intrusion cable while routing other cables.

### 7. PSU & Motherboard Connections
- Connect:
  - 24-pin main power
  - Two CPU power cables (8-pin, black/yellow)
  - Front panel power cable (long, black sheath, wide head, many pins — can be tricky)
  - PSU sensor cable (red/green/white/yellow)
- Order does not matter at this stage, but cables may need repositioning during final management.

### 8. Drives
- Install HDDs into brackets, align screw holes, and slide into bays.
- Label each drive with the correct bay number.
- Remove or replace certain stickers as required later.

### 9. Optic Modules
- Insert optic modules into the slots on the add-on card at the rear of the system.

### 10. Finishing
- Perform final cable management as tidy as possible.
- Close the system.
- Place the completed server on Memtest.

## Common Issues / Gotchas

- **SATA/NVMe issues** — Unreliable NVMe ports or OS incompatibility.
- **RAID card BIOS** — Sometimes requires updating before the system is stable.
- **Cloning issues** — Occasionally encountered during OS or disk image setup.
- **Client-dependent configs** — Some builds require the client to remote in and finish configuration (e.g., optic drive setup). This limits the ability to fully complete setup internally.
- **Remote access / network issues** — Problems with Ethernet port assignment (e.g., eth0 vs. mt0 designation differences).

## RAID & Cloning Notes

- **Accessing RAID utilities**
  - Some systems: RAID card BIOS is accessible through the system BIOS screen.
  - Other systems: RAID card has its own dedicated BIOS utility, accessed via hotkey during POST.
- **Cloning process**
  - Typically performed through the RAID card BIOS navigation.
  - Some systems allow running a script in the shell/OS for nearly instantaneous cloning.
- **Drive states / terminology**
  - **Degraded** — Array had a valid config but errored during initialization (e.g., one or more drives removed).
  - **Foreign / Foreign Body / Unconfigured Good** — Specific statuses indicating drives with mismatched or unrecognized configurations (requires deeper lookup).
- **Hybrid systems (HDD + SSD)**
  - Usually clone the HDDs (primary drives).
  - SSDs are only installed/configured when specifically requested by the client. The client typically remotes in to finalize SSD setup.

## Lessons Learned
- Always double-check CHA_FAN #1 connection to avoid loud fan ramp-up.
- Proper torque patterns and secure mounting of add-on cards prevent the majority of post-build issues.
- Documenting client-specific configuration requirements early avoids last-minute remote access surprises.
- Thorough final cable management and Memtest validation are critical before shipping.

**Status:**  This procedure was the current working standard for all server builds during tenure.
**Last Updated:** /16/2026