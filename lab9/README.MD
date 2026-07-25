# Program to Implement the Booth Algorithm

## 1. Objective

- To understand the Booth multiplication algorithm.
- To implement the Booth algorithm using a programming language.
- To perform multiplication of signed binary numbers.
- To analyze the working of Booth's algorithm.
- To verify the multiplication result through program execution.

---

## 2. Theory

**Booth's Algorithm** is an efficient algorithm used for multiplying signed binary numbers represented in **2's complement form**. It reduces the number of addition and subtraction operations required during multiplication, making it suitable for computer processors and digital systems.

The algorithm examines two consecutive bits of the multiplier (Q₀ and Q₋₁) and performs operations based on their values. After each operation, an arithmetic right shift is performed. This process continues until all bits of the multiplier have been processed.

### Rules of Booth's Algorithm

| Q₀ Q₋₁ | Operation |
|---------|-----------|
| 00 | No Operation |
| 01 | Add Multiplicand to Accumulator |
| 10 | Subtract Multiplicand from Accumulator |
| 11 | No Operation |

The steps of Booth's algorithm are:

1. Initialize the accumulator (A), multiplier (Q), multiplicand (M), and Q₋₁.
2. Check the values of Q₀ and Q₋₁.
3. Perform addition, subtraction, or no operation according to the rules.
4. Perform an arithmetic right shift on A, Q, and Q₋₁.
5. Repeat the process for the number of bits in the multiplier.
6. The final result is obtained by combining the contents of A and Q.

---

## 4. Applications

- Computer processors
- Arithmetic Logic Unit (ALU)
- Digital Signal Processing (DSP)
- Embedded systems
- Computer architecture
- Binary arithmetic operations
- High-speed multiplication circuits
- Digital communication systems
- Microprocessors
- Hardware design

---

## 5. Discussion

This experiment provided practical knowledge of implementing Booth's Algorithm for signed binary multiplication. The algorithm efficiently reduced the number of addition and subtraction operations by examining adjacent bits of the multiplier. The program execution produced the expected output, verifying the correctness of the implementation. Booth's Algorithm is widely used in modern processors because it provides faster multiplication of signed binary numbers and improves computational efficiency.

---

## 6. Conclusion

The program for implementing Booth's Algorithm was successfully executed and verified. The algorithm correctly performed multiplication of signed binary numbers using 2's complement representation. The obtained results matched the expected output, confirming the correctness of the implementation. This experiment improved the understanding of binary multiplication techniques and demonstrated the importance of Booth's Algorithm in computer architecture and digital system design.
