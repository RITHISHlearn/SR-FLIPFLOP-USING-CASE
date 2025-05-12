## SR-FLIPFLOP-USING-CASE

## AIM:

To implement SR flipflop using verilog and validating their functionality using their functional tables

## SOFTWARE REQUIRED:

Quartus prime

THEORY

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following   figure.

![image](https://github.com/user-attachments/assets/18be4f70-e857-4138-be15-e6cc92ff8595)


This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

 ![image](https://github.com/user-attachments/assets/702c4679-7091-480e-b609-6f107ae77750)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

 ![image](https://github.com/user-attachments/assets/e2a02856-2e1e-474d-9eeb-22264cbd734b)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

 ![image](https://github.com/user-attachments/assets/456a88cc-108a-4d97-87f6-8e7440f31154)


The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

## Procedure
 
1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

## PROGRAM
```
module ex6(S,R,clk,Q,Qbar);
input S,R,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=S|((~R)&Q);
Qbar=~Q;
end
endmodule
```

Developed by: RITHISH P

Reg No: 212223230173

## RTL LOGIC FOR FLIPFLOPS 

![image](https://github.com/user-attachments/assets/84896463-0287-4614-9aef-f82547f2d4f9)


## IMING DIGRAMS FOR FLIP FLOPS 

![image](https://github.com/user-attachments/assets/09635cab-3f58-4177-8229-1ed5e528a434)


## RESULTS 
Therefore the verilog HDL code has been successfully executed.
