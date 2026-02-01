# Fault Detection in SRAM using BIST

This repository presents a schematic-level implementation of a
Built-In Self-Test (BIST) architecture for fault detection in SRAM.

## Project Objective
The objective of this project is to design and verify a BIST-based
architecture capable of detecting common SRAM faults such as
stuck-at and transition faults using signature analysis.

## BIST Architecture Overview
The proposed SRAM BIST architecture consists of the following
functional blocks:

- Linear Feedback Shift Register (LFSR) for test pattern generation  
- Tri-State Inverter for controlled data driving during test mode  
- SRAM block as the memory under test  
- Multiple Input Signature Register (MISR) for response compaction  
- End-of-Test (EOT) Pulse Generator to indicate completion of BIST  
- Signature Comparator for PASS/FAIL decision  
- Integrated top-level schematic combining all blocks

## Fault Models Addressed
The following SRAM fault conditions are considered:

- Pass condition (fault-free operation)  
- Stuck-At-0 fault  
- Stuck-At-1 fault  
- Transition fault  

Fault detection is achieved by comparing the generated MISR signature
with a reference signature.

## Design Methodology
- Schematic-level design using Cadence Virtuoso
- Functional verification through signal-level observation
- Fault injection at schematic level to validate detection capability


## Tools Used
- Cadence Virtuoso – Schematic Editor

## Project Scope
- Focused on architectural and functional correctness
- Implemented and verified at schematic level only

## Limitations
- Physical layout, DRC, LVS, and post-layout simulations are not included
- Timing analysis and fault coverage metrics are not evaluated

## Conclusion
This project demonstrates the effectiveness of a BIST-based approach
for detecting stuck-at and transition faults in SRAM at the
schematic level using MISR-based signature comparison.

