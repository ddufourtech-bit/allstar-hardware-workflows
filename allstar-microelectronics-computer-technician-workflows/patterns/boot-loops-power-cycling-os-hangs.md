# Pattern: Boot Loops, Power Cycling & OS Hangs

**Status:** Common Failure Mode  
**Date:** May 2025

## Pattern
- **Boot Loops**: System attempts to start but fails to load OS and restarts (invalid/corrupt boot record, wrong boot device, PXE boot without server).
- **Power Cycling**: Powers on for a few seconds then shuts off (POST never reached) — usually failing PSU, motherboard short, or bad RAM.
- **OS Boot Hangs**: Corrupt OS, failing storage, BIOS misconfig (RAID vs AHCI, Secure Boot), or peripheral conflicts.

## Diagnostic Workflow & Fixes
1. Verify BIOS/UEFI boot order and disable PXE if not needed.
2. Check MBR/partition table on intended boot drive.
3. Test bare-minimum hardware (CPU + 1 DIMM, no drives).
4. Verify all power connections (24-pin, 8-pin CPU, GPU).
5. Test drive health, SATA cables, and BIOS storage settings.
6. Remove peripherals and test RAM one stick at a time.

## Lessons Learned
- Power cycling is almost always hardware (PSU/motherboard/RAM).
- Boot loops are frequently configuration related.

**Related Documents:**  
- [Storage Drive Failures](../storage-drive-failures.md)