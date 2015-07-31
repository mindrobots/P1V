# A brief overview of files in the HDL directory
# created 7-31-2015, Rick Post
# Please update as you add files
#
# General file extensions:
#  .cof - configuration files for the Quartus "Convert Programming Files" tool
#  .sdc - design constraint and timing constraint file
#  .qpf - Quartus project file
#  .qsf - Quartus pin mapping file - maps FPGA pins to symbols usable in verilog
#  .v - verilog code
#

altera.v - module to create a workable Altera PLL and clock 

BeMicroCV-A9.cof - 

BeMicroCV-A9_description.txt

BeMicroCV-A9.qsf - FPGA pin mapping for BeMicroCV-A9

BeMicroCV-A9.v - "top" verilog file for building a BeMicroCV-A9, includes P1V.v and 
                altera.v

BeMicroCV.cof

BeMicroCV.qsf - FPGA pin mapping for BeMicroCV

cog_alu.v - module to define standard P1V COG Arithmetic Logic Unit

cog_ctr.v - module to define standard P1V COG counter

cog_ram.v - module to define standard P1V COG RAM

cog.v - module to define standard P1V COG, includes cog_ram.v, cog_alu.v,
        cog_ctr.v and cog_vid.v

cog_vid.v - module to define standard P1V COG video components

DE0-Nano.cof

DE0-Nano.qsf - FPGA pin mapping for DE0-Nano

DE0-Nano.sdc

DE2-115.cof

DE2-115.qsf- FPGA pin mapping for DE2-115

DE2-115.sdc

dig.v - module to define digital logic and glue OUTSIDE of the COGs and HUB
        includes cog.v and hub.v - defines cnt, cog_led, hub bus, in/out/dir logic, etc.

features.v - macros for various features - currently has INVERT_COG_LEDS

fpga123_description.txt

fpga123.qsf - FPGA pin mapping for Parallax 1-2-3 FPGA

fpga123.v - "top" verilog file for building a Parallax 1-2-3 FPGA, includes P1V.v and 
                altera.v

hub_mem.v - module to define standard P1V HUB RAM includes load of HUB ROM from .hex files

hub_rom_high.hex - .hex images for standard P1V HUB ROM - included in hub_mem.v 

hub_rom_low.hex - .hex images for standard P1V HUB ROM - included in hub_mem.v

hub.v - module to define standard P1V HUB - includes HUB RAM plus defines busses, muxes and
        hub instructions (LOCKS, COGNEW, COGINIT, etc.)

P1V_Altera.qpf - Quartus project file - "standard" P1V build can be created by selecting 
                revisions from this file once it is opened in Quartus. Support for 
                standard P1V build on additional(new) boards should added to this file as 
                new revisions and the required files should be put in the HLD directory

p1v.v - module to build a standard P1V core - includes tim.v and dig.v

readme.txt - this file

tim.v - module to manage clock and export clk_pll and clk_cog and manage Propeller clk 

top.v - generic top file, used to build BeMicroCV,DE0-Nano and DE2-115 - this is the
        top.v file from the original Parallax P1V verilog. Any added boards
        should probably use custom top files based off of BeMicroCV-A9.v


