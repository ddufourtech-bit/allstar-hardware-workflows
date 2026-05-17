# Pattern: No POST / No Video

**Status:** Common Failure Mode  
**Date:** May 2025

## Pattern
- Most often indicates a failed motherboard.
- Other suspects: bad RAM or CPU.
- If no discrete GPU is present → onboard video may be in use.
- Rare case (seen once): bad onboard HDMI port caused no video.

## Diagnostic Workflow & Fixes
1. Confirm onboard vs. GPU presence.
   - GPU present: Try known-good card, reseat, verify PCIe power.
   - Onboard only: Check monitor/cable, look for POST LEDs or beep codes.
2. Reseat RAM (safe and quick first step).
3. Avoid pulling the CPU immediately (long process and risk of damage).
4. Motherboard is the most common point of failure.

## Lessons Learned
- Always start with simple reseats before swapping major components.
- Verify onboard video when no GPU is installed.

**Related Documents:**  
- [Motherboard Failures](../motherboard-failures.md)