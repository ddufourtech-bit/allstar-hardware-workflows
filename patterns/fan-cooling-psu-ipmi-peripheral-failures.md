# Pattern: Fan/Cooling, PSU, IPMI, NIC & PCIe Failures

**Status:** Common Peripheral & Component Failures  
**Date:** May 2025

## Fan / Cooling Failures
- Mechanical failure, bad cables/pins, wrong BIOS/IPMI config, dust, or liquid cooling pump/gasket issues.
- CHA_FAN1 not connected → system ramps all fans to 100%.

## PSU Failures
- No power, random shutdowns, capacitor issues, fan failure, coil whine.

## IPMI / BMC Failures
- No IPMI LED, unstable web UI, missing IP, sensor misreadings, lost credentials.

## NIC & PCIe Card Failures
- No link/activity, port-specific failures, speed/duplex mismatch, bad cables/slots, firmware/driver issues.

## Diagnostic Workflow & Fixes (Summary)
- Verify CHA_FAN1 and correct fan headers.
- Replace dead fans/cables/PSUs (never repair PSU).
- Reset/reflash BMC for IPMI issues.
- Reseat cables/cards, test in alternate slots, update firmware/drivers.
- Clean dust and verify airflow.

## Lessons Learned
- CHA_FAN1 logic and proper header placement prevent 90% of loud fan ramp-ups.
- Always check cables and seating before assuming a card or board is dead.

**Related Documents:**  
- [Random Shutdowns / Restarts](../random-shutdowns-restarts.md)