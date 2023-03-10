# Lab 1: GHDL and GTKWave
## Instructions
1. Go to the [GitHub repository](https://github.com/kevinwlu/dsd) of Digital System Design (DSD)  
    - Study VHDL and GHDL  
2. Go to the [GHDL](https://github.com/kevinwlu/dsd/tree/master/ghdl) folder  
    - Install GHDL and GTKWave  
    - Run the Half Adder example  
    - Run another example such as D Flip-Flop or 4-to-1 Multiplexer  
    - Document the results on your GitHub repository  
3. Exploration: [Icarus Verilog](https://en.wikipedia.org/wiki/Icarus_Verilog)
### Half [Adder](https://en.wikipedia.org/wiki/Adder_(electronics)) (Code from Prof. Lu's repo)
```$ ghdl -a ha.vhdl
$ ghdl -a ha_tb.vhdl
$ ghdl -e ha_tb
$ ghdl -r ha_tb --vcd=ha.vcd
ha_tb.vhdl:47:5:@5ns:(assertion error): Reached end of test
$ gtkwave ha.vcd
```
### [D Flip-Flop](https://electronicstopper.blogspot.com/2017/07/d-flip-flop-in-vhdl-with-testbench.html) (Code from Prof. Lu's repo)
```$ ghdl -a dff.vhdl
$ ghdl -a dff_tb.vhdl
$ ghdl -e dff_tb
$ ghdl -r dff_tb --vcd=dff.vcd
$ gtkwave dff.vcd
```
### [4-to-1 Multiplexer](https://allaboutfpga.com/vhdl-4-to-1-mux-multiplexer) (Code from Prof. Lu's repo)
```$ ghdl -a mux.vhdl
$ ghdl -a mux_tb.vhdl
$ ghdl -e mux_tb
$ ghdl -r mux_tb --vcd=mux.vcd
$ gtkwave mux.vcd
```
