# Pattern: Motherboard Failures

**Status:** Common Component Failure  
**Date:** May 2025

## Pattern
- Board won’t power or won’t POST.
- Common in Supermicro (rough PCI card handling, pulling cards while powered).
- Intermittent instability, dead slots (DIMM/PCIe/SATA), physical damage, or rare firmware corruption.

## Diagnostic Workflow & Fixes
- Most cases require RMA/repair.
- Exception: Bent pins can sometimes be carefully realigned.
- Inspect for physical damage (bent CPU pins, blown caps, cracked solder).

## Lessons Learned
- Rough handling of add-on cards is the leading cause of Supermicro board failures.

**Related Documents:**  
- [No POST / No Video](../no-post-no-video.md)