# 8-BIT-SHIFTER
An 8-bit cyclic shifter- A register that takes an input of 8 bits, and shift them according to another 3-bit input (you have 8 options of shifting: 0-7).
In computer structure which has a lot of registers, that chip can take a little part in the computing system.

Made of 24 Mux_1-2 components- Every Mux takes two different input bits (A and B), and according to a selection input bit (S), outputs one of them (the out is the information thats inside the selected bit) 

Truth Table of Mux:     A   B   S    0UT           
                        0   0   0     0
                        0   0   1     0
                        0   1   0     0
                        0   1   1     1
                        1   0   0     1
                        1   0   1     0
                        1   1   0     1
                        1   1   1     1
U can see here the schematic and silicon layout design of the mux component. Using the CMOS method (the transistor sizes was computed according to the worst case of resistence).


The Shifter is made out of 24 Muxes (3 rows of 8), and 3 Inverters (NOT-gate).
The first row takes every bit of the shifter input, and according to the LSB of the 3-bit input- shifts (or not) the 8-bit input by one.
The second row takes the output from the first row, and according to the middle bit of the 3-bit input- shifts (or not) the 8-bit input by 2.
The 3rd row takes...... from the second row, .........MSB...........shifts (or not) the 8-bit input by 4.

Together the input will shift according to the 3-bit input.

Example: 8-bit input: 00001111
         3-bit input: 011 - (3 shifts)
         output: 11100001
