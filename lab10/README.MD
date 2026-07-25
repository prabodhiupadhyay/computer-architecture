# Program to Implement the Non-Restoring Division Algorithm

## 1. Objective

- To study the Non-Restoring Division Algorithm.
- To implement the algorithm using a programming language.
- To perform binary division efficiently.
- To verify the division result through program execution.

---

## 2. Theory

The **Non-Restoring Division Algorithm** is a binary division technique used in digital computers. It performs division without restoring the previous remainder after every subtraction, making it faster than the restoring division algorithm.

The algorithm uses the **Accumulator (A)**, **Dividend (Q)**, and **Divisor (M)**. Depending on whether the accumulator is positive or negative, the divisor is either subtracted from or added to the accumulator. After each operation, a left shift is performed. At the end of the process, if the accumulator is negative, the divisor is added once more to obtain the correct remainder.

---

## 3. Simulation Result

The program was executed successfully, and the Non-Restoring Division Algorithm correctly calculated the quotient and remainder. The obtained output matched the expected division result, confirming the correctness of the implementation.

## 4. Applications

- Computer processors
- Arithmetic Logic Unit (ALU)
- Digital computers
- Embedded systems
- Binary arithmetic operations
- Computer architecture

---

## 5. Discussion

This experiment demonstrated the implementation of the Non-Restoring Division Algorithm for binary division. The program correctly generated the quotient and remainder while reducing unnecessary restore operations. The simulation verified the accuracy of the algorithm and showed its usefulness in high-speed digital systems.

---

## 6. Conclusion

The Non-Restoring Division Algorithm was successfully implemented and tested. The program produced the correct quotient and remainder, verifying the algorithm's correctness. This experiment improved the understanding of binary division techniques and their application in computer architecture and digital system design.
