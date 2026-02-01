# Schematic Circuits

This folder contains Cadence Virtuoso schematic-level designs developed for the project  
**Fault Detection in SRAM using Built-In Self-Test (BIST)**.

## Objective
The objective of these schematics is to implement and verify the functional blocks
required for SRAM fault detection using a BIST architecture at the schematic level.

## Included Schematic Blocks

### 1. LFSR (Linear Feedback Shift Register)
Generates pseudo-random test patterns used to perform write and read operations
on the SRAM during BIST execution.

### 2. Tri-State Inverter
Used to control signal driving during test mode and normal mode operation,
ensuring proper isolation and controlled data flow.

### 3. SRAM Block
Represents the memory under test where various fault conditions are targeted
using BIST-generated test patterns.

### 4. MISR (Multiple Input Signature Register)
Compacts the read data from the SRAM into a signature for fault detection
and response analysis.

### 5. End-of-Test (EOT) Pulse Generator
Generates an end-of-test signal indicating the completion of the BIST sequence.

### 6. Signature Comparator
Compares the generated MISR signature with a precomputed reference signature
to determine pass/fail status of the SRAM.

### 7. Integrated Top-Level Schematic
Integrates the LFSR, Tri-State Inverter, SRAM, MISR, End-of-Test Pulse Generator,
and Signature Comparator to form the complete BIST architecture.

## Design Tool
- Cadence Virtuoso – Schematic Editor

## Design Scope
- Schematic-level design and functional verification.
- Focused on architectural correctness and signal-level connectivity.

## Note
Physical layout, DRC, LVS, timing analysis, and post-layout simulations were not
performed as part of this project phase.
