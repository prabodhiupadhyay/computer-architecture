# Laboratory Report

## Title

**Introduction to VHDL Programming and Open-Source Simulation Environment**

## Objective

1. To understand the basics of VHDL (VHSIC Hardware Description Language).
2. To learn the structure and syntax of a VHDL program.
3. To develop and simulate simple digital circuits using VHDL.
4. To familiarize with an open-source simulation environment for hardware design verification.

## Theory

### VHDL Overview

VHDL (VHSIC Hardware Description Language) is a hardware description language used to model, design, and simulate digital systems. It allows designers to describe the behavior and structure of electronic circuits before implementing them on hardware such as FPGAs and ASICs.

VHDL supports:

* Behavioral modeling
* Dataflow modeling
* Structural modeling

A VHDL design generally consists of two main parts:

#### 1. Entity

The entity defines the input and output ports of a digital circuit.

#### 2. Architecture

The architecture describes the functionality or behavior of the circuit.

### Open-Source Simulation Environment

An open-source simulation environment provides tools for compiling and simulating VHDL designs without requiring commercial software licenses.

Common open-source tools include:

* GHDL (VHDL simulator)
* GTKWave (waveform viewer)

#### Advantages

* Free and accessible
* Cross-platform support
* Suitable for educational and research purposes
* Supports industry-standard VHDL code

## Apparatus/Software Required

* Computer with Linux/Windows operating system
* GHDL Simulator
* GTKWave Waveform Viewer
* Text Editor (VS Code, Notepad++, etc.)

## Procedure

### Part A: Writing a VHDL Program

1. Create a VHDL source file.
2. Define the entity with input and output ports.
3. Write the architecture describing the circuit behavior.
4. Save the file with a `.vhd` extension.

### Example: AND Gate

```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity AND_GATE is
    Port (
        A : in STD_LOGIC;
        B : in STD_LOGIC;
        Y : out STD_LOGIC
    );
end AND_GATE;

architecture Behavioral of AND_GATE is
begin
    Y <= A and B;
end Behavioral;
```

### Part B: Simulation

1. Analyze the VHDL file using GHDL.

```bash
ghdl -a and_gate.vhd
```

2. Elaborate the design.

```bash
ghdl -e AND_GATE
```

3. Run the simulation.

```bash
ghdl -r AND_GATE
```

4. Generate waveform data.

```bash
ghdl -r AND_GATE --vcd=wave.vcd
```

5. Open the waveform file using GTKWave.

```bash
gtkwave wave.vcd
```

## Observation

### Truth Table of AND Gate

| A | B | Y |
| - | - | - |
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

The simulation waveform verified that the output follows the logical AND operation for all input combinations.

## Result

The VHDL program for an AND gate was successfully developed and simulated using an open-source simulation environment. The simulation results matched the expected truth table, demonstrating the correctness of the design and the effectiveness of GHDL and GTKWave for digital circuit verification.

## Conclusion

This experiment introduced the fundamentals of VHDL programming and hardware description concepts. The use of open-source tools such as GHDL and GTKWave enabled successful compilation, simulation, and verification of a digital circuit design. The experiment provided practical experience in digital hardware modeling and simulation, which forms the basis for more complex FPGA and ASIC design projects.

## Precautions

1. Ensure proper VHDL syntax before compilation.
2. Verify port declarations and signal types.
3. Save files with the correct `.vhd` extension.
4. Check for compilation errors before simulation.
5. Use appropriate test cases to validate circuit behavior.
