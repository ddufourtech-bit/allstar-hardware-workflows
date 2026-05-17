# Pattern: Memory (DIMM) Failures

**Status:** Common Component Failure  
**Date:** May 2025

## Pattern
- Causes shutdowns, no POST, POST codes/beeps, or OS instability (crashes, panics, BSODs).

## Diagnostic Workflow & Fixes
1. Reseat DIMMs.
2. Test one stick at a time.
3. Try alternate slots.
4. Run Memtest86+ when possible.

## Lessons Learned
- Reseating and single-stick testing isolates bad DIMMs quickly and safely.

**Related Documents:**  
- [Boot Loops, Power Cycling & OS Hangs](../boot-loops-power-cycling-os-hangs.md)