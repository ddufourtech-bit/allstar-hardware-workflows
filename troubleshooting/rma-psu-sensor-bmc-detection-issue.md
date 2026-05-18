# RMA: PSU Port #2 Not Detected in BMC

**Status:** Resolved via Firmware Update  
**Date Received:** 2025-05-06  
**Motherboard:** Supermicro H13SSL-N  

## Problem Summary
In BMC/IPMI, only PSU Port #1 was visible. Port #2 showed no data.

## Troubleshooting Performed
1. Verified both PSUs function independently in both ports.
2. Swapped PSUs between ports (solo and tandem) — issue followed the port.
3. RMA'd suspected PSU sensor module.
4. Received replacement — issue persisted.
5. Tested with known-good motherboard — issue still present.
6. Updated BMC Firmware + BIOS via IPMI.
7. Retested: both PSUs now detected correctly.
8. Began Memtest.

## Root Cause
Outdated BMC Firmware / BIOS causing sensor communication failure (not hardware fault).

## Resolution
Firmware and BIOS update resolved detection on both ports. System passed Memtest.

## Lessons Learned
- When sensor issues survive multiple hardware swaps, always check firmware/BIOS versions before further RMA.
- Document exact firmware versions before and after updates.


**Status:** Closed  
**Last Updated:** May 16, 2026
