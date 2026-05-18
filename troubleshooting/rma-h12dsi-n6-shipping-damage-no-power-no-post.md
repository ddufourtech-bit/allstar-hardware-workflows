# RMA: H12DSi-N6 Shipping Damage – No Power / No POST

**Status:** Resolved (RMA Issued)  
**Date:** February–March 2025  
**Motherboard:** Supermicro H12DSi-N6

## Problem Summary
Multiple H12DSi-N6 motherboards arrived with visible shipping damage and would not power on or POST.

## Findings
- Physical damage to chipset ICs U6 and U11 (chipped corners/edges)
- Bent DisplayPort, damaged serial port, and bent RAM slots (P1/P2 DIMM areas)
- Loose chassis fan brackets and scuffed PCIe slot area
- System would not power on at all — safety hazard prevented further testing
- CPUs and RAM tested good on known-good board

## Root Cause
Severe shipping damage during transit (packaged upside-down / improper handling).

## Resolution
- Documented all damage with photos
- Submitted RMA to Supermicro with full evidence package
- Board returned for replacement

## Validation
- Replacement boards arrived and passed full Memtest + burn-in
- No further power-on or POST issues

## Lessons Learned
- Always photograph incoming boards immediately and before any power-on attempt
- Never attempt to power a board with visible chipset or slot damage
- Shipping damage claims require clear photographic evidence of U6/U11 area
