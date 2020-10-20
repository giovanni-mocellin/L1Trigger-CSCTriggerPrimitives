# L1Trigger-CSCTriggerPrimitives

This repository holds look-up-tables which map a pattern number and a 12-bit comparator code onto an unsigned 4-bit position offset and a 5-bit slope. In the current form, there are 5 patterns (0 through 4) and 4096 comparator codes. LUTs are also available with floating point values (for reference). A third set of LUTs convert the Run-1/2 patterns to Run-3 patterns.

The firmware dataword for each pattenr and comparator code is 18 bits long:
   - [8:0] is quality (set all to 0 for now)
   - [12:9] is slope value
   - [13] is slope sign
   - [17:14] is position offset
