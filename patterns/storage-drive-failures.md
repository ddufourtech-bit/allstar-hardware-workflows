# Pattern: Storage Drive (HDD / SSD / NVMe) Failures

**Status:** Common Component Failure  
**Date:** May 2025

## Pattern
- System fails to boot OS.
- Drive not detected in BIOS.
- I/O errors, freezes, SMART errors, intermittent detection, or slow performance.

## Diagnostic Workflow & Fixes
1. Reseat/replace cables.
2. Run SMART / vendor health check.
3. Test drive in another system.
4. Replace drive if confirmed bad.

## Lessons Learned
- Cables and seating issues cause the majority of “drive not detected” cases.

**Related Documents:**  
- [Boot Loops, Power Cycling & OS Hangs](../boot-loops-power-cycling-os-hangs.md)