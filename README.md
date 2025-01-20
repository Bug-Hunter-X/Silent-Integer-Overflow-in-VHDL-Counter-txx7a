# Silent Integer Overflow in VHDL Counter

This repository demonstrates a subtle bug in VHDL code where an integer counter silently overflows without generating a warning or error during simulation. This can lead to unexpected behavior in the synthesized hardware.

## Bug Description
The `buggy_counter.vhdl` file contains a counter that increments an integer. When the counter reaches its maximum value (15), it silently wraps around to 0.  This behavior might not be immediately obvious during simulation and could lead to issues in the real hardware.

## Solution
The `fixed_counter.vhdl` file provides a corrected version that uses a more robust approach to handle potential overflow.  This could involve checking for maximum value and handling the condition explicitly or using a different data type (like `unsigned`).

## How to reproduce
1. Simulate `buggy_counter.vhdl` with your preferred VHDL simulator.
2. Observe the counter behavior when it reaches 15.  Note the silent rollover.
3. Simulate `fixed_counter.vhdl` and observe the improved behavior.
