# Build Procedure: MSI MEG X870E GODLIKE – High-End Dual-GPU Water-Cooled Tower

**Status:** Completed & Verified  
**Date:** June 2025  
**Chassis:** High-airflow black tower case  
**Motherboard:** MSI MEG X870E GODLIKE  
**Base Procedure:** Follows [Standard Tower Build Procedure](../standard-tower-build-procedure.md)

## Overview
This build followed the standard tower workflow with the following enhancements:
- Dual GPU configuration
- Custom water cooling loop with pump
- MSI EZ Control Hub + Magnetic EZ Bridge fan/ARGB control system
- RAID 0 storage configuration
- CPU overclocking with multi-stage stability testing

## Build Process (Tower Standard + Specific Additions)

### 1. Chassis & Motherboard Preparation
- Followed standard tower chassis preparation and motherboard prep (CPU, RAM, heatsink).
- Installed CPU, RAM, and M.2 SSD(s) on the bench before chassis installation.

### 2. Motherboard Installation into Chassis
- Attached the USB 3.0 cable to the motherboard before mounting.
- Mounted the motherboard into the chassis **before** installing the water pump (water pumps are bulky and tower cases offer limited working space once the board is mounted).

### 3. Water Cooling Installation
- Installed the water block and pump assembly onto the CPU after the motherboard was secured.
- Mounted the radiator with fans in optimal push/pull configuration.
- Routed and secured all tubing and pump power/control cables.

### 4. MSI EZ Control Hub & Magnetic EZ Bridge Installation
- Installed the standalone EZ Control Hub (Breakout Hub) inside the chassis.
- Connected up to 7 chassis fans, ARGB lighting strips, and thermal probes directly to the hub.
- Ran a single main ribbon cable from the hub to the Magnetic EZ Bridge on the edge of the motherboard.
- The EZ Bridge magnetically attaches to the board edge and consolidates all fan, lighting, and sensor data into one streamlined connection.
- Connected a dedicated SATA power cable directly from the PSU to the EZ Control Hub.

**Important Notes on the EZ System:**
- The hub relies on the MSI SCM (System Control) driver for full functionality in BIOS and MSI Center.
- The bridge cable must be pushed in extremely firmly — it has no traditional locking clip. Loose contact can cause fans to default to 100% speed and loss of control in the OS/BIOS.

### 5. Dual GPU Installation
- Installed both GPUs in the primary and secondary PCIe slots.
- Connected all required supplemental power cables.

### 6. Storage Configuration (RAID 0)
- Configured the NVMe drives in RAID 0 within the BIOS.
- Performed multiple stability and performance tests to validate the array.

### 7. Overclocking & Final Tuning
- Applied CPU overclock after confirming baseline stability.
- Ran a series of stress tests and benchmarks to dial in voltages, clocks, and cooling performance.

### 8. Cable Management & Final Validation
- Followed standard tower cable management (small cables first, power cables next, front-panel last).
- Powered on and confirmed successful POST.
- Entered BIOS to set fan curves, enable XMP, configure RAID, update time/date, and fine-tune the overclock.
- Booted into the OS and performed full system stress testing under load.

## Lessons Learned
- Mounting the motherboard before the water pump provides significantly more working room in a tower chassis.
- The MSI EZ Control Hub + Magnetic EZ Bridge system greatly reduces cable clutter but requires careful seating of the bridge cable.
- RAID 0 and overclocking both demand thorough multi-stage testing to ensure long-term stability.
- Pre-planning cable routing around the water loop and dual GPUs prevents rework later.

## Evidence
- Bench preparation (CPU/RAM/M.2)
- Motherboard mounted in chassis
- Water pump integration
- EZ Control Hub and Magnetic EZ Bridge cabling
- Dual GPU and RAID 0 configuration
- Final system with clean cable management and RGB synchronization

**Status:** Fully Operational – Stable, high-performance system with advanced cooling, storage, and fan control.  
**Related Documents:**  
- [Standard Tower Build Procedure](01-build-procedures/standard-tower-build-procedure.md),(04-evidence/msi-godlike-custom-pc-build)