# LAB REPORT

## Title

Realization of Basic Logic Gates Using VHDL

## Objective

To design, implement, and verify the operation of basic logic gates (AND, OR, NOT, NAND, NOR, XOR, and XNOR) using VHDL.

## Apparatus/Software Required

* Computer System
* VHDL Simulator (ModelSim/Xilinx Vivado/Quartus Prime)
* VHDL Compiler

## Theory

Logic gates are the fundamental building blocks of digital circuits. They perform logical operations on one or more binary inputs and produce a binary output. VHDL (VHSIC Hardware Description Language) is used to describe and model digital systems.

The basic logic gates are:

* AND Gate: Output is HIGH only when all inputs are HIGH.
* OR Gate: Output is HIGH when at least one input is HIGH.
* NOT Gate: Produces the complement of the input.
* NAND Gate: Complement of AND operation.
* NOR Gate: Complement of OR operation.
* XOR Gate: Output is HIGH when inputs are different.
* XNOR Gate: Output is HIGH when inputs are the same.

## VHDL Code

```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity logic_gates is
    Port (
        A : in STD_LOGIC;
        B : in STD_LOGIC;
        AND_OUT  : out STD_LOGIC;
        OR_OUT   : out STD_LOGIC;
        NOT_OUT  : out STD_LOGIC;
        NAND_OUT : out STD_LOGIC;
        NOR_OUT  : out STD_LOGIC;
        XOR_OUT  : out STD_LOGIC;
        XNOR_OUT : out STD_LOGIC
    );
end logic_gates;

architecture Behavioral of logic_gates is
begin
    AND_OUT  <= A and B;
    OR_OUT   <= A or B;
    NOT_OUT  <= not A;
    NAND_OUT <= A nand B;
    NOR_OUT  <= A nor B;
    XOR_OUT  <= A xor B;
    XNOR_OUT <= A xnor B;
end Behavioral;
```

## Procedure

1. Open the VHDL simulation software.
2. Create a new project and add the VHDL source file.
3. Write and compile the VHDL code.
4. Simulate the design using different input combinations.
5. Observe and verify the outputs obtained for each logic gate.
6. Compare the outputs with the corresponding truth tables.

## Truth Table

| A | B | AND | OR | NAND | NOR | XOR | XNOR |
| - | - | --- | -- | ---- | --- | --- | ---- |
| 0 | 0 | 0   | 0  | 1    | 1   | 0   | 1    |
| 0 | 1 | 0   | 1  | 1    | 0   | 1   | 0    |
| 1 | 0 | 0   | 1  | 1    | 0   | 1   | 0    |
| 1 | 1 | 1   | 1  | 0    | 0   | 0   | 1    |

NOT Gate Truth Table:

| A | NOT A |
| - | ----- |
| 0 | 1     |
| 1 | 0     |

## Observation

The simulated outputs matched the expected outputs obtained from the truth tables of the respective logic gates.

## Result

The basic logic gates (AND, OR, NOT, NAND, NOR, XOR, and XNOR) were successfully realized and verified using VHDL. The simulation results were found to be correct according to the corresponding truth tables.

## Conclusion

The experiment demonstrated the implementation of basic logic gates using VHDL. The behavior of each gate was successfully verified through simulation, confirming the correctness of the VHDL design.

