# L1Trigger-CSCTriggerPrimitives

## CCLUT

This repository holds lookup-tables which map a pattern number and a 12-bit comparator code onto an unsigned 4-bit position offset and a 5-bit slope. In the current form, there are 5 patterns (0 through 4) and 4096 comparator codes. LUTs are also available with floating point values (for reference). A third set of LUTs convert the Run-1/2 patterns to Run-3 patterns. The .mem files are those which will be loaded into VERILOG firmware.

The firmware dataword for each pattern and comparator code is 18 bits long:
   - [8:0] is quality (set all to 0 for now)
   - [12:9] is slope value
   - [13] is slope sign
   - [17:14] is position offset

## GEM-CSC LUTs

This repository also holds lookup-tables that map GEM readout channels (pad) onto 1/8-strip CSC channels, and that map GEM roll numbers onto CSC wiregroups. LUTs are provided for ME1/1 and ME2/1, for even and odd. In the case of ME1/1, separate LUTs are present for ME1/a and ME1/b strips. A single LUT is foreseen for the wiregroups. The .mem files are those which will be loaded into VERILOG firmware.

* map GEM pad onto CSC 1/8-strip number
   - GEMCSCLUT_pad_es_ME1a_even.txt (start at CSC strip 64, or 1/8-strip 512)
   - GEMCSCLUT_pad_es_ME1a_odd.txt  (start at CSC strip 64, or 1/8-strip 512)
   - GEMCSCLUT_pad_es_ME1b_even.txt
   - GEMCSCLUT_pad_es_ME1b_odd.txt
   - GEMCSCLUT_pad_es_ME21_even.txt
   - GEMCSCLUT_pad_es_ME21_odd.txt

* map GEM roll onto CSC minimum and maximum wiregroup number
   - GEMCSCLUT_roll_max_wg_ME11_even.txt
   - GEMCSCLUT_roll_max_wg_ME11_odd.txt
   - GEMCSCLUT_roll_max_wg_ME21_even.txt
   - GEMCSCLUT_roll_max_wg_ME21_odd.txt
   - GEMCSCLUT_roll_min_wg_ME11_even.txt
   - GEMCSCLUT_roll_min_wg_ME11_odd.txt
   - GEMCSCLUT_roll_min_wg_ME21_even.txt
   - GEMCSCLUT_roll_min_wg_ME21_odd.txt

## CSC ME1/1 LUTs

* map wiregroup onto min and max half-strip number that it crosses
   - CSCLUT_wg_min_hs_ME1a.txt
   - CSCLUT_wg_max_hs_ME1a.txt
   - CSCLUT_wg_min_hs_ME1a_ganged.txt
   - CSCLUT_wg_max_hs_ME1a_ganged.txt
   - CSCLUT_wg_min_hs_ME1b.txt
   - CSCLUT_wg_max_hs_ME1b.txt
