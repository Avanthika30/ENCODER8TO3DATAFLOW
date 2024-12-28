### ENCODER 8TO3 DATAFLOW Modelling

**AIM:**

To implement  Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:** Quartus prime

**THEORY**
An encoder is a combinational circuit that reduces multiple inputs into a smaller number of outputs. It performs the reverse operation of a decoder. An 8-to-3 encoder converts eight inputs (D₀ to D₇) into a 3-bit binary output (Y₂, Y₁, Y₀). Only one of the inputs is assumed to be active (logic HIGH) at any given time.

**Encoder 8 To 3**

The 8 to 3 line Encoder is also known as Octal to Binary Encoder. In 8 to 3 line encoder, there is a total of eight inputs, i.e., D0, D1, D2, D3, D4, D5, D6, and D7 and three outputs, i.e., A0, A1, and A2. In 8-input lines, one input-line is set to true at a time to get the respective binary code in the output side. Below are the block diagram and the truth table of the 8 to 3 line encoder.

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/0bc242c1-eb9e-4c47-afe5-30428470efc3)

Figure 01  Block Diagram of Encoder 8 * 3

**Truth Table**

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/35496b14-ae6e-4cd1-9abd-d6736b576575)

The logical expression of the term A0, A1, and A2 are as follows:

A0 = D1 + D3 + D5 + D7

A1 = D2 + D3 + D6 + D7

A2 = D4 + D5 + D6 + D7

Logical circuit of the above expressions is given below:

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/95acaee6-c873-4c75-89eb-ef09fb158053)

Figure 02  Encoder 8 * 3

**Procedure**
Understand Functionality:
Inputs: D₀ to D₇ (8 lines), Outputs: Y₂, Y₁, Y₀ (3 lines).
One input HIGH produces a 3-bit binary output.
Derive Logic Equations
Open Quartus:
Create a new project named Encoder8to3.
Add a Verilog file.
Write Verilog Code
Use ModelSim or Quartus Waveform Viewer to verify results.
**PROGRAM**

/* Program for Encoder 8 To 3 in Dataflow Modelling and verify its truth table in quartus using Verilog programming. 

Developed by:Avanthika.B RegisterNumber:24900424
*/
```
module binary_encoder(
  input [7:0] D,
  output [2:0] y);
  assign y[2] = D[4] | D[5] | D[6] | D[7];
  assign y[1] = D[2] | D[3] | D[6] | D[7];
  assign y[0] = D[1] | D[3] | D[5] | D[7];
endmodule
```
**RTL LOGIC FOR Encoder 8 To 3 in Dataflow Modelling**

![image](https://github.com/user-attachments/assets/9c2c35c7-24d8-48f1-b852-9e4eb1a9e6f9)

**TIMING DIGRAMS FOR Encoder 8 To 3 in Dataflow Modelling**

![ep 5 1](https://github.com/user-attachments/assets/9f38d0eb-93e2-43d6-abe8-f0511f840018)

**RESULTS**
The Encoder 8 To 3 in Dataflow Modelling using verilog is implemented and validated their functionality using their functional tables.



