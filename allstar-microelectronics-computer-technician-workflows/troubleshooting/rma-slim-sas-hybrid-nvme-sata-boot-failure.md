# RMA / TS: SlimSAS Hybrid NVMe/SATA Path – Linux Boot Failure (ATA Errors)

**Status:** Resolved (Hardware Path Change)  
**Date:** May 2025

## Problem Summary
System detected HDDs in BIOS but failed to boot Linux with repeated WRITE FPDMA QUEUED, ATA bus errors, and PHY/link resets.

## Findings
- Issue only occurred when using SlimSAS hybrid NVMe/SATA ports + breakout cables with SATA HDDs
- Identical systems with dedicated SATA ports worked fine
- BIOS POST detection passed; failure happened during OS kernel storage initialization

## Root Cause
Redriver timing instability on hybrid SlimSAS path when used with SATA HDD boot media

## Resolution
1. Removed HDDs from SlimSAS hybrid path
2. Reconnected using dedicated onboard SATA ports and standard cables
3. Reconfigured boot path to traditional SATA controller

## Validation
- BIOS detection consistent
- OS boot completed without ATA errors
- Multiple reboot cycles passed

## Lessons Learned
- Never use hybrid NVMe/SATA SlimSAS ports for SATA HDD boot drives on this platform

**Evidence:** Linux boot logs and dmesg output (in evidence/ folder)