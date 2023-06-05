# 8:1 MULTIPLEXER USING VERILOG
## AIM :
To implement 16:1 multiplexer using verilog and validate its outputs
## HARDWARE REQUIRED :
– PC, Cyclone II , USB flasher
## SOFTWARE REQUIRED:
Quartus prime
## THEORY
What is a Multiplexer ?
The multiplexer is a device that has multiple inputs and single line output. The select lines determine which input is connected to the output, and also increase the amount of data that can be sent over a network within a certain time. It is also called a data selector.

The single-pole multi-position switch is a simple example of a non-electronic circuit of the multiplexer, and it is widely used in many electronic circuits. The multiplexer is used to perform high-speed switching and is constructed by electronic components.A multiplexer, often abbreviated as "MUX," is a digital electronic device that combines multiple input signals into a single output signal. It is commonly used in digital circuitry and communication systems to transmit multiple data streams over a single channel or to select one of several input sources for further processing.

A multiplexer has several input lines, usually denoted as "n" lines, and one or more control lines, typically denoted as "s" lines. The number of control lines determines the number of input lines that can be selected. For example, with a 2-bit control line, you can select one of four input lines (2^2 = 4). The selected input line is then connected to the output line.

image

16 to 1 Multiplexer
In the 16 to 1 multiplexer, there are total of 16 inputs, i.e., A0, A1, …, A16, 4 selection lines, i.e., S0, S1, S2, and S3 and single output, i.e., Y. On the basis of the combination of inputs that are present at the selection lines S0, S1, and S2, one of these 16 inputs will be connected to the output. The block diagram and the truth table of the 16×1

A 16:1 multiplexer is a digital logic component that has 16 input lines, one output line, and four control or select lines. It is also known as a 16-input multiplexer. The select lines determine which input line is connected to the output line.

The control or select lines are usually binary and represent a unique combination of values from 0 to 15 (in binary form). Each combination of select line values corresponds to one of the 16 input lines. The selected input line is then routed to the output line.

In the truth table above, S3, S2, S1, and S0 represent the four select lines, and I15 to I0 represent the input lines. The selected input line, determined by the select lines' binary combination, is passed to the output line.The 16:1 multiplexer is often used in digital systems to select one out of 16 inputs and route it to the output based on the control signals provided by the select lines.

16 mux

## PROCEDURE
Step 1
Create a project with required entities.

Step 2
Create a module along with file name for Multiplexer .

Step 3
Type the code in the created module and run the stimulation.

Step 4
After it get successfully runned get the respective RTL outputs.

Step 5
Create university program(VWF) for getting timing diagram.

Step 6
Give the respective inputs for timing diagram and get the results.
## PROGRAM
```
module muxx(a,s,y);
input[7:0]a;
input[2:0]s;
output reg y;
always @ (a,s)
begin
   case(s)
   3'b000:y=a[0];
	3'b001:y=a[1];
	3'b010:y=a[2];
	3'b011:y=a[3];
	3'b100:y=a[4];
	3'b101:y=a[5];
	3'b110:y=a[6];
	3'b111:y=a[7];
   endcase
end
endmodule
```
## LOGIC DIAGRAM
![image](https://github.com/Reebak04/Simulation-project--Digital-Electronics/assets/118364993/da1d527f-729f-49cd-996b-b8ca2b8d8772)
## NETLIST DIAGRAM
![image](https://github.com/Reebak04/Simulation-project--Digital-Electronics/assets/118364993/a7fde9c4-b1f1-43a2-be5a-75423513b34c)
## TIMING DIAGRAM
![image](https://github.com/Reebak04/Simulation-project--Digital-Electronics/assets/118364993/a181bca1-95ee-4f0e-919a-66560b190131)
## TRUTH TABLE
![image](https://github.com/Reebak04/Simulation-project--Digital-Electronics/assets/118364993/6d5101f8-da2d-463a-881a-d1305a46e8b1)
## RESULT
Thus the implementation of 8 : 1 Multiplexer are verified.
