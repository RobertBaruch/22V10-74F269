# 22V10-74F269
An implementation of the 74F269 bidirectional counter ([datasheet](https://archive.org/details/74f269Philips)) on a 22V10 GAL.

counter.pld is the original .pld file. You can use WinCUPL from Microchip to compile it to a JEDEC (.jed) file.

COUNTER.jed is the JEDEC file that a chip programmer reads to program the chip. It can be programmed to an ATF22V10 chip, or a Lattice 22V10 GAL.

COUNTER.txt contains the expanded, minimized logic equations, and the pinout.

This is the pinout, which DOES NOT MATCH the 74F269 due to limitations in the GAL.

                               ______________
                              |   Counter    |
                      CLK x---|1           24|---x Vcc                      
                       D0 x---|2           23|---x Q2                       
                       D1 x---|3           22|---x Q3                       
                       D2 x---|4           21|---x Q4                       
                       D3 x---|5           20|---x Q5                       
                       D4 x---|6           19|---x Q6                       
                       D5 x---|7           18|---x Q7                       
                       D6 x---|8           17|---x Q1                       
                       D7 x---|9           16|---x Q0                       
                     !CEP x---|10          15|---x !TC                      
                     !CET x---|11          14|---x UP                       
                      GND x---|12          13|---x !PE                      
                              |______________|

![Breadboarded 16-bit counter](breadboard-16bit.jpg)
