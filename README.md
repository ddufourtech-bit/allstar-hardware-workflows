# Allstar Microelectronics – Computer Technician Workflows & Documentation

**Professional production documentation created and maintained while working as a Computer Technician at Allstar Microelectronics.**

This repository contains the internal technical knowledge base I built and continuously improved for server build processes, troubleshooting, RMA handling, and daily hardware operations.

## Purpose
- Document standardized build procedures, diagnostic tools, error patterns, and RMA processes for enterprise server hardware.
- Serve as a living reference for the hardware team.
- Demonstrate real-world hardware troubleshooting, systematic diagnostics, documentation discipline, and process improvement in a high-volume production environment.

**This is paid professional work — not a homelab.**

## Repository Contents

| Section                  | Description |
|--------------------------|-----------|
| **`build-procedures/`**  | Standardized LEGO, Tower, and Server build procedures + specific high-end builds |
| **`checklists/`**        | Reusable checklists for new devices, post-change verification, etc. |
| **`evidence/`**          | Redacted original RMA forms, raw notes, and build photos<br>**Note:** ASUS PRO, MSI Godlike, and SlimSAS evidence each have their own subfolder with a dedicated README.md |
| **`patterns/`**          | Recurring error patterns and fixes (7 reference guides) |
| **`standards/`**         | Platform-specific guidelines (SlimSAS hybrid ports, storage topology, cabling, etc.) |
| **`troubleshooting/`**   | Individual ticket-style runbooks from real production RMA and in-house cases |
| **`changelog.md`**       | Record of updates and additions to the documentation |

### Build Procedures
- [Standard LEGO Build Procedure](build-procedures/standard-lego-build-procedure.md)
- [Standard Tower Build Procedure](build-procedures/standard-tower-build-procedure.md)
- [Standard Server Build Procedure](build-procedures/standard-server-build-procedure.md)
- [MSI MEG X870E GODLIKE – Dual-GPU Water-Cooled Tower](build-procedures/msi-meg-x870e-godlike-dual-gpu-water-cooled-tower-build.md) *(evidence: [evidence/msi-godlike-custom-pc-build](evidence/msi-godlike-custom-pc-build))*
- [ASUS PRO WS W680-ACE IPMI + Water-Cooled LEGO](build-procedures/asus-pro-ws-w680-ace-ipmi-water-cooled-lego-build.md) *(evidence: [evidence/asus-pro-ws-w680-ace-ipmi-water-cooled-lego-build](evidence/asus-pro-ws-w680-ace-ipmi-water-cooled-lego-build))*

### Notable Troubleshooting Cases
- [RMA – H12DSi-N6 Shipping Damage – No Power / No POST](troubleshooting/rma-h12dsi-n6-shipping-damage-no-power-no-post.md)
- [RMA – Supermicro Vendor Repair – Damaged ICs on H12DSi-N6](troubleshooting/rma-supermicro-repair-damaged-ics-h12dsi-n6.md)
- [RMA – H13SSL-N PSU Sensor / BMC Detection Issue](troubleshooting/rma-h13ssl-n-psu-sensor-bmc-detection-issue.md)
- [SlimSAS Hybrid NVMe/SATA Path – Linux Boot Failure (ATA Errors)](troubleshooting/rma-slim-sas-hybrid-nvme-sata-boot-failure.md) *(evidence: [evidence/slim-sas-hybrid-nvme-sata-linux-boot-failure](evidence/slim-sas-hybrid-nvme-sata-linux-boot-failure))*
- [RMA – Shipping Damage – Bent RAM Slots & Physical Ports](troubleshooting/rma-shipping-damage-bent-ram-slots-ports.md)
- [Pattern – Shipping Damage – Multiple H12DSi-N6 Units](troubleshooting/rma-shipping-damage-pattern-multiple-units.md)
- [RMA – No Display – RAM Slot Physical Damage](troubleshooting/rma-no-display-ram-slot-damage.md)
- [RMA – IPMI No LED / No POST (H12DSi-N6)](troubleshooting/rma-ipmi-no-led-no-post.md)

### Error Patterns Reference
- [No POST / No Video](patterns/no-post-no-video.md)
- [Random Shutdowns or Restarts](patterns/random-shutdowns-restarts.md)
- [Boot Loops, Power Cycling & OS Hangs](patterns/boot-loops-power-cycling-os-hangs.md)
- [Memory (DIMM) Failures](patterns/memory-failures.md)
- [Storage Drive Failures](patterns/storage-drive-failures.md)
- [Motherboard Failures](patterns/motherboard-failures.md)
- [Fan/Cooling, PSU, IPMI, NIC & PCIe Failures](patterns/fan-cooling-psu-ipmi-peripheral-failures.md)

## Key Skills Demonstrated
- Systematic root-cause analysis across multiple identical systems
- Isolation of subtle signal-integrity and timing issues (redriver chips, hybrid storage paths)
- Vendor RMA coordination and follow-through with photographic evidence
- Creation of clear, actionable, reusable technical documentation
- Cross-testing of hardware paths (motherboard vs. backplane vs. cable)
- Production-level attention to detail in high-volume server builds and repairs

## How to Use This Repository
- Start with the build procedures.
- Use `patterns/` for quick reference on recurring issues.
- Dive into `troubleshooting/` for specific real-world cases.
- Check `evidence/` subfolders for supporting photos (each has its own README.md).

**Related Labs**  
[AD DS Homelab – Windows Server 2025](https://github.com/ddufourtech-bit/ad-ds-homelab-windows-server-2025)  
[Azure Lab](https://github.com/ddufourtech-bit/azure-lab) *(Networking & Security)*

---

**Last Updated:** May 16, 2026  
**Author:** David Dufour  
**License:** All content is for portfolio demonstration purposes only.