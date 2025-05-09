# D-FLIPDLOP-NEGEDGE
# NAME: Preethi.K
# Register no: 212224240118

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

1.Open Quartus → Create a New Project.

2.Write Verilog Code for D Flip-Flop using negedge clk.

3.Save the Code (e.g., D_FF.v) → Add it to the project.

4.Set Top-Level Module in project settings.

5.Compile the project → Done!

**PROGRAM**
```
module dflip(D,Clock,reset,Q);
input D,reset,Clock;
output reg Q;
always @ (negedge Clock)
if(!reset)
Q <= 0;
else
Q <= D;
endmodule

```

**RTL LOGIC FOR FLIPFLOPS**

![Screenshot 2025-05-09 155745](https://github.com/user-attachments/assets/a5ca6c45-832e-4b0c-8618-6baa79659d1a)


**TIMING DIGRAMS FOR FLIP FLOPS**

![Screenshot 2025-05-09 155805](https://github.com/user-attachments/assets/b782715d-33fa-4fc5-89d6-6d9f7f4d3393)

**RESULTS**
Thus the D-filpflop was successfully implemented and verified.
