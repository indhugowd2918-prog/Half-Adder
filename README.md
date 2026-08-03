
`timescale 1ns/1ps

module half_adder_tb;

reg A;
reg B;

wire Sum;
wire Carry;

half_adder uut (
    .A(A),
    .B(B),
    .Sum(Sum),
    .Carry(Carry)
);

initial begin

$display("A B | Sum Carry");
$display("----------------");

A=0; B=0; #10;
$display("%b %b |  %b    %b",A,B,Sum,Carry);

A=0; B=1; #10;
$display("%b %b |  %b    %b",A,B,Sum,Carry);

A=1; B=0; #10;
$display("%b %b |  %b    %b",A,B,Sum,Carry);

A=1; B=1; #10;
$display("%b %b |  %b    %b",A,B,Sum,Carry);

$finish;

end

endmodule
# Half Adder using Verilog

## Overview

A Half Adder is a combinational logic circuit that adds two single-bit binary numbers. It has two inputs (A and B) and produces two outputs:

- Sum (S)
- Carry (C)

## Truth Table

| A | B | Sum | Carry |
|---|---|-----|-------|
| 0 | 0 |  0  |   0   |
| 0 | 1 |  1  |   0   |
| 1 | 0 |  1  |   0   |
| 1 | 1 |  0  |   1   |

## Logic Equations

- Sum = A XOR B
- Carry = A AND B

## Files

- `half_adder.v` – Verilog design
- `half_adder_tb.v` – Testbench
- `simulation_result.png` – Simulation waveform

## Software Used

- Xilinx Vivado / ModelSim / Icarus Verilog
- GTKWave (optional)

## Expected Output

| A | B | Sum | Carry |
|---|---|-----|-------|
|0|0|0|0|
|0|1|1|0|
|1|0|1|0|
|1|1|0|1|

## Author

Your Name
# Half Adder using Verilog

## Overview

A Half Adder is a combinational logic circuit that adds two single-bit binary numbers. It has two inputs (A and B) and produces two outputs:

- Sum (S)
- Carry (C)

## Truth Table

| A | B | Sum | Carry |
|---|---|-----|-------|
| 0 | 0 |  0  |   0   |
| 0 | 1 |  1  |   0   |
| 1 | 0 |  1  |   0   |
| 1 | 1 |  0  |   1   |

## Logic Equations

- Sum = A XOR B
- Carry = A AND B

## Files

- `half_adder.v` – Verilog design
- `half_adder_tb.v` – Testbench
- `simulation_result.png` – Simulation waveform

## Software Used

- Xilinx Vivado / ModelSim / Icarus Verilog
- GTKWave (optional)

## Expected Output

| A | B | Sum | Carry |
|---|---|-----|-------|
|0|0|0|0|
|0|1|1|0|
|1|0|1|0|
|1|1|0|1|

## Author

Your Name
module half_adder(
    input A,
    input B,
    output Sum,
    output Carry
);

assign Sum = A ^ B;
assign Carry = A & B;

endmodule
