# VHDL Counter Overflow Bug
This repository demonstrates a common error in VHDL code: improper handling of counter overflow.  The `buggy_counter.vhdl` file contains a counter that might not reset correctly under certain conditions. The `fixed_counter.vhdl` file provides a corrected version.  The bug arises from a potential issue in how the counter is reset within the process.

## Bug Description
The `buggy_counter` entity implements a simple 4-bit counter. However, the reset condition in the process might not always reset the counter to zero, leading to unexpected behavior or continued counting from previous value. This could be caused by the sensitivity list (clk,rst) which might not reset the counter to zero under certain scenarios.