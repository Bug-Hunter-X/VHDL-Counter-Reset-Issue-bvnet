# VHDL Counter with Reset Issue

This repository demonstrates a common error in VHDL code related to counter reset behavior. The `buggy_counter.vhd` file contains a counter that doesn't correctly reset when the reset signal is active after reaching the maximum count. The `fixed_counter.vhd` file provides a corrected version.

## Bug Description
The buggy counter fails to reset to zero when the reset signal (`rst`) is high after the count reaches its maximum value (15 in this case).  This can lead to unpredictable behavior and incorrect functionality in a larger system. 

## Bug Solution
The corrected version, `fixed_counter.vhd`, addresses this issue by ensuring that the reset signal (`rst`) is always checked in the process, regardless of the counter value.  This ensures that the counter resets whenever the reset signal is asserted.
