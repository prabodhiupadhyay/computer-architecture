# **Lab Report: VHDL Code for Combinational Circuits – Comparator**

## **Objective**

* To study the concept and working principle of combinational logic circuits.
* To understand the operation of a digital comparator.
* To learn how comparators compare two binary numbers.
* To understand the implementation of a comparator using VHDL.
* To verify the output of the comparator through simulation.

---

# **Theory**

A **comparator** is a combinational logic circuit that compares two binary numbers and determines their relationship. It indicates whether one binary number is **greater than**, **less than**, or **equal to** another binary number. Unlike sequential circuits, combinational circuits do not require memory elements or clock signals. Their outputs depend only on the current inputs.

Comparators are widely used in digital systems such as arithmetic logic units (ALUs), microprocessors, digital signal processing, memory address comparison, sorting circuits, and control systems. They are essential components wherever decision-making based on binary values is required.

A comparator accepts two binary inputs, generally represented as **A** and **B**, and produces three outputs:

* **A > B** : High when A is greater than B.
* **A = B** : High when A is equal to B.
* **A < B** : High when A is less than B.

Only one of these outputs becomes logic HIGH (1) at a time.

### Working Principle

The comparator compares corresponding bits of the two input numbers starting from the most significant bit (MSB). If the MSBs are equal, it proceeds to compare the next significant bits until a difference is found. The first unequal pair of bits determines whether A is greater than or less than B. If all corresponding bits are equal, the equality output becomes HIGH.

### Types of Comparators

1. **1-bit Comparator**

   * Compares two single-bit binary inputs.

2. **2-bit Comparator**

   * Compares two 2-bit binary numbers.

3. **4-bit Comparator**

   * Compares two 4-bit binary numbers.
   * Can also be cascaded to compare larger binary numbers.

### Boolean Equations (1-bit Comparator)

Let the inputs be **A** and **B**.

**Equality Output**

[
A = B = A'B' + AB
]

**Greater Than Output**

[
A > B = AB'
]

**Less Than Output**

[
A < B = A'B
]

Where:

* **A'** = Complement of A
* **B'** = Complement of B

### Truth Table

| A | B | A>B | A=B | A<B |
| - | - | --- | --- | --- |
| 0 | 0 | 0   | 1   | 0   |
| 0 | 1 | 0   | 0   | 1   |
| 1 | 0 | 1   | 0   | 0   |
| 1 | 1 | 0   | 1   | 0   |

### Applications of Comparator

* Arithmetic Logic Units (ALUs)
* Microprocessors and Microcontrollers
* Digital Control Systems
* Address Comparison in Memory
* Sorting and Searching Algorithms
* Digital Measurement Instruments
* Data Processing Systems
* Error Detection Circuits

### Comparator in VHDL

VHDL provides an efficient way to model comparator circuits. Relational operators such as **=**, **>**, and **<** are commonly used to compare binary inputs. During simulation, the comparator checks the input values and activates the appropriate output signal. Since a comparator is a combinational circuit, the outputs change immediately whenever the inputs change.


# **Discussion**

The comparator is one of the fundamental combinational logic circuits used in digital electronics. Its main function is to compare two binary inputs and determine whether they are equal, greater than, or less than each other. The VHDL implementation simplifies the design process by allowing comparison through relational operators rather than constructing the circuit using individual logic gates.

The simulation confirms that only one output remains HIGH for any input combination, demonstrating the correct operation of the comparator. The design is simple, reliable, and can easily be expanded to compare larger binary numbers by increasing the input width or cascading multiple comparators. Comparators play an important role in processors, digital communication systems, and embedded applications where fast decision-making is required.


# **Conclusion**

The experiment successfully demonstrated the operation of a combinational comparator using VHDL. The comparator correctly compared two binary inputs and generated the appropriate output indicating whether one input was greater than, less than, or equal to the other. The theoretical concepts were verified through simulation, showing that the output depends only on the present input values. This experiment improved the understanding of combinational logic design, digital comparison techniques, and the practical use of VHDL in designing and verifying digital circuits.

