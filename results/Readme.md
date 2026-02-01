# Results

This folder presents the observed results of the SRAM BIST architecture
based on schematic-level fault detection.

## Evaluated Fault Conditions

### 1. Pass Condition
- The SRAM operates correctly under BIST execution.
- Generated MISR signature matches the reference signature.
- Signature comparator indicates a **PASS** status.

### 2. Fail Condition
- A fault is introduced in the SRAM block during BIST operation.
- Generated MISR signature differs from the reference signature.
- Signature comparator indicates a **FAIL** status.

### 3. Stuck-At-0 Fault
- Memory node is permanently stuck at logic ‘0’.
- BIST-generated test patterns fail to write or read logic ‘1’.
- MISR captures a faulty signature, resulting in **FAIL** detection.

### 4. Stuck-At-1 Fault
- Memory node is permanently stuck at logic ‘1’.
- BIST-generated test patterns fail to write or read logic ‘0’.
- MISR captures a faulty signature, resulting in **FAIL** detection.

### 5. Transition Fault
- Memory cell fails to transition between logic ‘0’ and logic ‘1’.
- Fault is observed during consecutive write and read operations.
- MISR signature mismatch confirms **FAULT DETECTION**.

## Result Interpretation
- PASS or FAIL status is determined using MISR signature comparison.
- Fault detection is based on signature mismatch at the end of BIST execution.

## Design Level
- Results are obtained from schematic-level functional verification only.

## Conclusion
The BIST architecture successfully detects stuck-at and transition faults
in SRAM at the schematic level using MISR-based signature comparison.
