# RMA: H13SSL-N PSU Sensor / BMC Detection Issue

**Status:** Resolved (Firmware Update)  
**Date:** February 2025  
**Motherboard:** Supermicro H13SSL-N

## Problem Summary
PSU Port #2 not detected in BMC; sensor module swaps did not resolve.

## Findings
- BMC did not detect PSU in secondary power slot
- Multiple sensor module swaps performed
- Issue persisted until firmware update

## Root Cause
Outdated BMC / BIOS firmware

## Resolution
- Updated BMC and BIOS firmware
- Verified both PSU ports now detected correctly

## Validation
- Both PSU sensors visible and reporting in IPMI
- Full system power-on and stability confirmed

## Lessons Learned
- Firmware updates often resolve intermittent sensor/BMC detection issues before hardware replacement

**Evidence:** 5005168-10 and 5005168-20 RMA forms (in evidence/ folder)