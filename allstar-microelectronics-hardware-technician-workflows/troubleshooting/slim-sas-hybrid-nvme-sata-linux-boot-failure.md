# Server Troubleshooting: SlimSAS Hybrid NVMe/SATA Path Causing Linux Boot / ATA Errors

**Status:** Resolved  
**Issue Type:** Storage Path / Boot Failure (Linux-specific)  
**Platform:** Supermicro Servers (H12SSW / H13 series and similar)  
**Affected Components:** SATA HDDs connected via SlimSAS NVMe/SATA hybrid ports + breakout cables  

## Problem Summary
Systems failed to reliably boot or install Linux-based operating systems (Debian 12, Ubuntu 25).  

The system would sometimes reach a login prompt (`Debian GNU/Linux 12 ... tty1`) before entering a repeating error loop. Windows 10 booted successfully on the same hardware, making the issue appear OS-specific at first.

## Symptoms
- Repeated ATA/I/O errors during OS initialization:
  - `WRITE FPDMA QUEUED`
  - ATA bus error
  - `Emask 0x10`
  - `SError`
  - `PHYRdyChg`, `CommWake`, `DevExch`
- Intermittent I/O failures
- Inconsistent behavior by drive bay/port
- BIOS detected all drives correctly in every bay

## Scope
- Affected: 2 out of 8 otherwise identical systems
- 6 systems booted Debian normally
- Issue only manifested when using **SlimSAS hybrid NVMe/SATA ports** with breakout cables for SATA HDDs
- Traditional dedicated SATA ports did not exhibit the problem

## Environment
- **Motherboard:** Supermicro H12SSW / H13 series (AMD EPYC Rome)
- **Storage Topology:** CPU → PS8743 redriver → SlimSAS hybrid ports → breakout cable → SATA HDDs
- **OS Tested:** Debian 12 (Bookworm), Ubuntu 25 installer, Windows 10 (working)
- **IPMI:** No hardware faults logged

## Troubleshooting Performed
1. Compared 8 identical systems side-by-side.
2. Swapped HDDs, SlimSAS cables, backplanes, and motherboards.
3. Tested drives/cables from faulty systems on known-good systems (and vice versa).
4. Observed issue followed the **motherboard + SlimSAS hybrid path**, not individual drives or cables.
5. Confirmed BIOS POST detection worked, but OS-level storage initialization failed.
6. Reproduced during Ubuntu 25 installation.

## Findings
- BIOS consistently detected drives regardless of bay.
- Errors only occurred on the hybrid SlimSAS NVMe/SATA path using breakout cables with SATA HDDs.
- Traditional SATA ports/cables worked reliably.
- H12SSW block diagram shows SlimSAS ports routed through redriver chips, adding complexity and reducing signal margin compared to direct SATA paths.
- Issue was **not** caused by failed HDDs, corrupted OS, or firmware mismatch.

## Root Cause
**Hybrid NVMe/SATA SlimSAS ports + breakout cables** introduced timing and signal integrity instability through the redriver during sustained OS/kernel storage initialization.  
BIOS detection succeeded, but the longer Linux storage subsystem initialization exposed the instability (Windows was more tolerant).

## Resolution
1. Removed all SATA HDD connections from SlimSAS hybrid NVMe/SATA ports and breakout cables.
2. Reconnected drives using **dedicated onboard SATA ports** and standard SATA cables.
3. Updated boot order to use the traditional SATA controller.
4. Saved configuration and retested.

## Validation
- BIOS continued to detect all drives correctly.
- OS storage subsystem initialized cleanly with no ATA bus errors.
- Full Debian 12 and Ubuntu 25 boot/install completed successfully.
- Multiple reboot cycles passed without recurrence.
- System reached stable login prompt (`Debian GNU/Linux 12 ... tty1`).

## Lessons Learned
- Hybrid SlimSAS/NVMe-SATA paths, while convenient for mixed storage, can introduce subtle timing issues with SATA HDD workloads during OS boot.
- Always validate storage paths with full OS initialization (not just BIOS POST).
- Prefer dedicated SATA cabling for boot/OS drives on hybrid-controller platforms.
- Cross-testing motherboards vs. backplanes/cables is essential to isolate path-related faults.

## Prevention
- Establish and document storage connection standards per motherboard/chassis type.
- Avoid using hybrid SlimSAS paths for primary SATA HDD boot drives.
- Test new storage topologies with target OS (especially Linux) before deployment.

**Closure Notes**  
This was a hardware path / signal integrity issue, not an OS or driver problem. Permanent fix achieved by switching to traditional SATA connectivity.

**Status:** Closed — Resolved via hardware path correction  
**Last Updated:** 5-16-2026
