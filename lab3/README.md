# LAB REPORT

## Title

Implementation of Combinational Circuits (Encoder and Decoder) Using VHDL

## Objective

To design, simulate, and verify the operation of Encoder and Decoder combinational circuits using VHDL.

## Theory

### Combinational Circuits

Combinational circuits are digital circuits whose outputs depend only on the present input values. They do not contain memory elements.

### Encoder

An encoder is a combinational circuit that converts one active input line into a coded binary output.

#### Truth Table of 4-to-2 Encoder

| D3 | D2 | D1 | D0 | Y1 | Y0 |
| -- | -- | -- | -- | -- | -- |
| 0  | 0  | 0  | 1  | 0  | 0  |
| 0  | 0  | 1  | 0  | 0  | 1  |
| 0  | 1  | 0  | 0  | 1  | 0  |
| 1  | 0  | 0  | 0  | 1  | 1  |

### Decoder

A decoder is a combinational circuit that converts binary information from n input lines to a maximum of 2ⁿ output lines.

#### Truth Table of 2-to-4 Decoder

| A1 | A0 | Y3 | Y2 | Y1 | Y0 |
| -- | -- | -- | -- | -- | -- |
| 0  | 0  | 0  | 0  | 0  | 1  |
| 0  | 1  | 0  | 0  | 1  | 0  |
| 1  | 0  | 0  | 1  | 0  | 0  |
| 1  | 1  | 1  | 0  | 0  | 0  |

## VHDL Code

### 4-to-2 Encoder

```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity Encoder is
    Port (
        D : in STD_LOGIC_VECTOR(3 downto 0);
        Y : out STD_LOGIC_VECTOR(1 downto 0)
    );
end Encoder;

architecture Behavioral of Encoder is
begin
    process(D)
    begin
        case D is
            when "0001" => Y <= "00";
            when "0010" => Y <= "01";
            when "0100" => Y <= "10";
            when "1000" => Y <= "11";
            when others => Y <= "00";
        end case;
    end process;
end Behavioral;
```

### 2-to-4 Decoder

```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity Decoder is
    Port (
        A : in STD_LOGIC_VECTOR(1 downto 0);
        Y : out STD_LOGIC_VECTOR(3 downto 0)
    );
end Decoder;

architecture Behavioral of Decoder is
begin
    process(A)
    begin
        case A is
            when "00" => Y <= "0001";
            when "01" => Y <= "0010";
            when "10" => Y <= "0100";
            when "11" => Y <= "1000";
            when others => Y <= "0000";
        end case;
    end process;
end Behavioral;
```

## Procedure

1. Open the VHDL simulation software (Vivado/ModelSim/Xilinx ISE).
2. Create a new project.
3. Write the VHDL code for Encoder and Decoder.
4. Compile the design and remove any errors.
5. Simulate the circuit using different input combinations.
6. Verify the outputs with the truth tables.

## Observation

### Encoder Results

| Input (D3 D2 D1 D0) | Output (Y1 Y0) |
| ------------------- | -------------- |
| 0001                | 00             |
| 0010                | 01             |
| 0100                | 10             |
| 1000                | 11             |

### Decoder Results

| Input (A1 A0) | Output (Y3 Y2 Y1 Y0) |
| ------------- | -------------------- |
| 00            | 0001                 |
| 01            | 0010                 |
| 10            | 0100                 |
| 11            | 1000                 |

## Result

The VHDL implementation of the 4-to-2 Encoder and 2-to-4 Decoder was successfully designed, simulated, and verified. The obtained outputs matched the expected truth tables.

## Conclusion

The experiment demonstrated the design and implementation of combinational circuits using VHDL. The Encoder correctly converted active input lines into binary codes, while the Decoder generated the corresponding output line based on the binary input.

