Lab Report
Title: VHDL Code for Sequential Circuits: Flip-Flops

1. Objective 🎯
To design and implement sequential circuits using VHDL.

To model basic flip-flops (SR, D, JK, T) and verify their functionality through simulation.

To understand the behavior of flip-flops as fundamental building blocks in digital systems.

2. Theory 📘
Flip-flops are bistable devices that store one bit of information. They are the basic memory elements in sequential logic.

SR Flip-Flop: Set-Reset, simplest form.

D Flip-Flop: Data or Delay, transfers input to output on clock edge.

JK Flip-Flop: Generalized SR with toggling capability.

T Flip-Flop: Toggle, changes state on each clock pulse.

In VHDL, flip-flops are modeled using process blocks sensitive to clock signals.

3. Apparatus ⚙️
Software: Xilinx ISE / ModelSim / Vivado

Hardware (optional): FPGA board (e.g., Spartan-6, Artix-7)

VHDL compiler and simulator

4. Procedure 🧪
1
Set Up Environment
Info
Prepare the VHDL simulation environment.

Install and open Xilinx ISE/ModelSim

Create a new VHDL project

Define entity and architecture for flip-flops

2
Write VHDL Code
Success
Implement flip-flop logic using process blocks.

Use process(clk) for sequential behavior

Define input/output ports (D, J, K, T, Q)

Apply conditional statements for flip-flop logic

3
Compile and Simulate
Recommended
Verify correctness of the code.

Run syntax check and compile

Apply testbench with clock pulses

Observe waveform outputs

4
Analyze Results
Warning
Compare simulated outputs with theoretical truth tables.

Check SR flip-flop for invalid states

Verify D flip-flop follows input

Confirm JK toggling behavior

Ensure T flip-flop alternates states

5
Implement on FPGA
Optional
Deploy design on hardware for real-time verification.

Synthesize design for FPGA

Generate bitstream

Program FPGA board and test outputs

5. Observations 📊
Waveforms matched expected truth tables for all flip-flops.

SR flip-flop showed indeterminate state when both inputs were high.

D flip-flop correctly latched input at clock edge.

JK flip-flop toggled as expected when J=K=1.

T flip-flop alternated output on each clock pulse.

6. Conclusion ✅
VHDL successfully modeled sequential circuits.

Flip-flops behaved according to theoretical definitions.

This experiment reinforced the importance of flip-flops in memory and control circuits.
