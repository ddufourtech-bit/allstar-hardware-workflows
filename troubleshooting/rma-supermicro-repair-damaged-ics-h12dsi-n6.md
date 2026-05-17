# RMA: Supermicro Vendor Repair – Damaged ICs on H12DSi-N6

**Status:** Resolved (Repaired & Returned)  
**Date:** March–April 2025  
**Motherboard:** Supermicro H12DSi-N6 (Rev 1.02)

## Problem Summary
Board arrived with visible IC damage and was submitted for vendor-level repair.

## Findings
- Damaged ICs: U11 (primary), U6, KU9, and shorted capacitors
- No POST, no IPMI LED activity on arrival
- Cburn test passed after component-level repair
- BIOS and BMC firmware updated during repair
- Full LAN boot test with dual EPYC 7303 CPUs passed

## Root Cause
Physical damage to critical chipset ICs (likely from shipping or handling)

## Resolution
- Submitted to Supermicro for component-level repair
- Board repaired, firmware updated, and fully retested by vendor

## Validation
- Cburn test: Pass
- LAN boot with dual CPUs: Pass
- PCIe RAID card test: Pass
- FRU/DMI verification: Pass

## Lessons Learned
- Component-level repair on H12DSi-N6 is viable when damage is limited to U6/U11 area
- Always request firmware updates during vendor RMA

**Evidence:** Supermicro Repair Report RI250304049 series (in evidence/ folder)