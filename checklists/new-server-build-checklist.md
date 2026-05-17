# New Server Build Checklist

**Allstar Microelectronics Hardware Technician Reference**  
**Last Updated:** May 16, 2026

**Work Order / Device Name:**  
**Date:**  

## Pre-Build
- [ ] Work order and BOM verified
- [ ] All components inspected for shipping damage
- [ ] Firmware/BIOS versions checked against standards

## Build Steps
- [ ] Chassis prepared and standoffs installed
- [ ] Motherboard seated and all power cables connected
- [ ] CPU, RAM, and heatsink installed correctly
- [ ] Storage connected using proper cabling (dedicated SATA preferred)
- [ ] All fans connected (CHA_FAN1 rules followed)
- [ ] Cabling dressed and secured

## Power-On & Testing
- [ ] First power-on successful
- [ ] BIOS POST completed – all hardware detected
- [ ] Memtest86 run (minimum 4 passes)
- [ ] IPMI/BMC access verified
- [ ] Storage paths validated (no SlimSAS hybrid issues with SATA HDDs)

## Final Verification
- [ ] Full reboot cycle passed
- [ ] Build checklist signed off
- [ ] Photos of any anomalies taken
- [ ] System ready for imaging / shipping

**Notes / Deviations:**