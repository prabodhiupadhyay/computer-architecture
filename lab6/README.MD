# **Lab Report: VHDL Code for Combinational Circuits – Code Converter**

## **Objective**

* To understand the concept of combinational logic circuits.
* To study the working principle of digital code converters.
* To implement a code converter using VHDL.
* To simulate and verify the functionality of the code converter.
* To gain practical knowledge of VHDL programming for combinational circuits.

---

# **Theory**

## **Introduction**

Combinational circuits are digital logic circuits whose outputs depend only on the current input values. They do not contain memory elements or feedback paths, making their outputs independent of previous input states. These circuits are fundamental building blocks in digital electronics and are used in applications such as arithmetic operations, multiplexing, encoding, decoding, and code conversion.

A **code converter** is a combinational circuit that converts data from one digital code into another while preserving the represented information. Different coding systems are used in digital electronics to improve reliability, simplify circuit design, or reduce transmission errors. Code converters automatically translate one code format into another, making communication between different digital devices possible.

VHDL (Very High-Speed Integrated Circuit Hardware Description Language) is widely used to model, simulate, and implement combinational circuits. It allows designers to verify the functionality of a code converter before implementing it on programmable hardware such as FPGAs.

---

## **Combinational Circuits**

A combinational circuit is formed by connecting logic gates such as AND, OR, NOT, NAND, NOR, XOR, and XNOR. The output of the circuit is determined solely by the present combination of input values.

### Characteristics of Combinational Circuits

* Outputs depend only on present inputs.
* No memory or storage elements are used.
* No clock signal is required.
* Simple and fast operation.
* Easy to design and simulate using VHDL.

---

## **Code Converter**

A code converter converts one binary code into another according to predefined logic equations. It ensures that the numerical value remains unchanged while the coding format changes.

Some commonly used code converters are:

* Binary to Gray Code Converter
* Gray Code to Binary Converter
* BCD to Excess-3 Converter
* Excess-3 to BCD Converter
* Binary to BCD Converter

The conversion process is achieved using Boolean expressions implemented through combinational logic gates.

---

## **Working Principle**

The converter receives binary input signals and processes them using combinational logic. Based on the selected conversion method, the logic circuit generates the corresponding output code. Since there are no memory elements, the output changes immediately whenever the input changes.

In VHDL, the conversion logic is described using concurrent signal assignments or processes. A testbench is then used to apply different input combinations and verify the correctness of the generated outputs through simulation waveforms.

---

## **Applications of Code Converters**

* Digital communication systems
* Computer systems
* Embedded systems
* Digital display units
* Data encoding and decoding
* FPGA and ASIC design
* Industrial control systems

---

## **Simulation**

Simulation is performed to verify that the VHDL design produces the expected output for every input combination.

The simulation process includes:

1. Writing the VHDL code for the code converter.
2. Creating a testbench with different input combinations.
3. Compiling the design.
4. Running the simulation.
5. Viewing the waveform output.
6. Comparing the results with the expected code conversion.

Simulation helps identify logical errors before hardware implementation, making the design process more efficient and reliable.

---

# **Discussion**

In this experiment, a combinational code converter was designed and simulated using VHDL. The simulation demonstrated that the output code changed correctly according to the applied input combinations. The absence of memory elements ensured that the output responded immediately to input changes. The experiment also provided practical experience in writing VHDL descriptions, compiling the design, creating a testbench, and analyzing simulation waveforms. Overall, the experiment strengthened the understanding of combinational logic and digital code conversion techniques.

---

# **Conclusion**

The experiment successfully demonstrated the design and simulation of a combinational code converter using VHDL. The simulation results verified that the converter accurately transformed the input code into the desired output code for all tested input combinations. This experiment enhanced the understanding of VHDL programming, combinational circuit design, and digital code conversion. It also emphasized the importance of simulation in verifying digital circuits before implementing them on hardware.

