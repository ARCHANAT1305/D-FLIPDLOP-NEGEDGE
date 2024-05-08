# EXPERIMENT NO: 8 D-FLIPDLOP-NEGEDGE

## AIM:
To implement  D flipflop using verilog and validating their functionality using their functional tables

## SOFTWARE REQUIRED:
Quartus prime

## THEORY

### D Flip-Flop

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

## Procedure
1. Inputs:
D: Data input. This is the value that will be stored in the flip-flop on the rising edge of the clock.
Clock: Clock signal. The flip-flop operates on the falling edge of this signal.
Reset: Reset signal. When asserted (typically high), it resets the flip-flop's output to 0.
2. Output:
Q: Flip-flop output. This holds the value of D after the clock edge.
Operation:
At every falling edge of the Clock signal (negedge Clock), the following actions occur:
a. If the reset signal is asserted (!reset):
Set the output Q to 0, regardless of the value of D.
b. If the reset signal is not asserted:
3. Set the output Q to the value of D.
4. End of procedure.


## PROGRAM

 Program for flipflops and verify its truth table in quartus using Verilog programming.   
 Developed by: ARCHANA T  
 RegisterNumber:212223240013
 
 module d_flipflop(D,Clock,reset,Q);  
input D,reset,Clock;  
output reg Q;  
always @ (negedge Clock)  
if(!reset)    
Q <= 0;   
else  
Q <= D;  
endmodule  


## RTL LOGIC FOR FLIPFLOPS
![d flip flop diagram](https://github.com/ARCHANAT1305/D-FLIPDLOP-NEGEDGE/assets/145975189/255691fd-80ac-42d5-9cfa-1811938e424a)


## TIMING DIGRAMS FOR FLIP FLOPS
![d flip flop waveform](https://github.com/ARCHANAT1305/D-FLIPDLOP-NEGEDGE/assets/145975189/64da7159-7f02-45b0-9a7a-d8a3e75a1e6e)


## RESULTS
Thus the program executed successfully.
