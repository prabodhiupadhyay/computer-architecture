# Lab Report: 

#Title

VHDL Code for Combinational Circuits (MUX and DEMUX)

## Aim

To design and implement Multiplexer (MUX) and Demultiplexer (DEMUX) using VHDL and verify their functionality through simulation.

## Theory

### Multiplexer (MUX)

A Multiplexer is a combinational circuit that selects one of several input signals and forwards it to a single output line based on the select inputs.

A 2:1 Multiplexer has:

* Inputs: A, B
* Select Line: S
* Output: Y

Truth Table:

| S | Y |
| - | - |
| 0 | A |
| 1 | B |

### Demultiplexer (DEMUX)

A Demultiplexer is a combinational circuit that takes a single input and routes it to one of several outputs according to the select line.

A 1:2 Demultiplexer has:

* Input: D
* Select Line: S
* Outputs: Y0, Y1

Truth Table:

| S | Y0 | Y1 |
| - | -- | -- |
| 0 | D  | 0  |
| 1 | 0  | D  |

## VHDL Code

### 2:1 Multiplexer

```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity MUX2X1 is
    Port (
        A, B : in STD_LOGIC;
        S    : in STD_LOGIC;
        Y    : out STD_LOGIC
    );
end MUX2X1;

architecture Behavioral of MUX2X1 is
begin
    Y <= A when S = '0' else B;
end Behavioral;
```

### 1:2 Demultiplexer

```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity DEMUX1X2 is
    Port (
        D    : in STD_LOGIC;
        S    : in STD_LOGIC;
        Y0   : out STD_LOGIC;
        Y1   : out STD_LOGIC
    );
end DEMUX1X2;

architecture Behavioral of DEMUX1X2 is
begin
    Y0 <= D when S = '0' else '0';
    Y1 <= D when S = '1' else '0';
end Behavioral;
```

## Result

The VHDL implementation of the 2:1 Multiplexer and 1:2 Demultiplexer was successfully designed and verified. The simulation results matched the expected truth tables, confirming the correct operation of both combinational circuits.

## Conclusion

The experiment demonstrated the design and implementation of basic combinational circuits using VHDL. The Multiplexer correctly selected one input based on the select line, while the Demultiplexer correctly routed the input signal to the desired output.
