# Design Overview

This document explains how the project is designed from an
object-oriented perspective.

---

## High-Level Flow
1. Read audio data from a WAV file
2. Convert raw data into samples
3. Apply noise reduction logic
4. Convert samples back into audio data
5. Write the output WAV file

---

## Planned Classes

### AudioReader
- Reads WAV files from disk
- Extracts audio samples
- Hides file format details from the rest of the system

---

### NoiseReducer
- Contains logic to reduce noise
- Works only on numerical samples
- Independent of file handling

---

### AudioWriter
- Writes processed samples back to a WAV file
- Responsible only for output format

---

## Responsibilities
Each class has a single responsibility.
This makes the system:
- Easier to understand
- Easier to test
- Easier to extend in the future

---

## Why This Design
Separating responsibilities allows:
- Unit testing of noise logic without file I/O
- Easy replacement of noise reduction algorithms
- Cleaner debugging and maintenance

This design follows basic SOLID and OOPS principles.

