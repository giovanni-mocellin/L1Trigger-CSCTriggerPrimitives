# L1Trigger-CSCTriggerPrimitives

This repository holds look-up-tables which, in their current form, map a 12-bit comparator code onto a floating point number. That can either be a position offset or a slope. In the current form, there are 5 patterns (0 through 4) and 4096 comparator codes. For the position offset, there is an ideal case and a realistic case. The ideal case does not take into account a global offset from alignment effects, while the realistic case does. In future versions, the values in the look-up-tables will be translated from floating point to unsigned int. 
