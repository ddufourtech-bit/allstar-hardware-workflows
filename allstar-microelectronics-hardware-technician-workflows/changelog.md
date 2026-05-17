# Changelog

All notable changes to this repository will be documented in this file.

## [Unreleased] - 2026-05-16

### Added
- Full `build-procedures/` folder with standardized workflows:
  - `standard-lego-build-procedure.md`
  - `standard-tower-build-procedure.md`
  - `standard-server-build-procedure.md`
  - `msi-meg-x870e-godlike-dual-gpu-water-cooled-tower-build.md` (with MSI EZ Control Hub details)
  - `asus-pro-ws-w680-ace-ipmi-water-cooled-lego-build.md`
- `patterns/` folder with 7 detailed error pattern reference guides:
  - No POST / No Video
  - Random Shutdowns or Restarts
  - Boot Loops, Power Cycling & OS Hangs
  - Memory (DIMM) Failures
  - Storage Drive Failures
  - Motherboard Failures
  - Fan/Cooling, PSU, IPMI, NIC & PCIe Failures
- `troubleshooting/` folder with 8 high-quality production RMA and in-house tickets (H12DSi-N6 shipping damage, Supermicro vendor repairs, H13SSL-N PSU/BMC issues, SlimSAS hybrid boot failures, etc.)
- `checklists/` folder with 4 reusable checklists:
  - New LEGO Build Completion Checklist
  - New Tower Build Completion Checklist
  - Post-Build Verification Checklist
  - RMA Intake & Documentation Checklist
- `standards/` folder with 5 platform-specific standards:
  - SlimSAS Hybrid Port Usage Standards
  - Fan Header and Cooling Standards
  - Cabling & Cable Management Standards
  - CPU Installation & Pin Protection Standards
  - RMA Photography & Documentation Standards
- Updated main `README.md` with complete table of contents, links to all new files, and correct evidence paths (`04-evidence/asus-pro/`, `04-evidence/msi/`, `04-evidence/slim-sas/`)

### Changed
- Reorganized evidence folders for ASUS PRO, MSI Godlike, and SlimSAS cases into dedicated subfolders under `04-evidence/`
- Standardized all Markdown files to consistent formatting, cross-linking, and professional tone

### Initial Repository Setup
- Created core structure for Allstar Microelectronics Hardware Technician documentation
- Converted raw Section 1–3 PDFs and RMA forms into structured, searchable Markdown

**Last Updated:** May 16, 2026  
**Author:** David Dufour