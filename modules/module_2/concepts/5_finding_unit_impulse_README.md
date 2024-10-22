## Linear Shift Invariance System: Finding Impulse Response

This document provides an explanation on how to determine the impulse response \( h(x) \) in a **Linear Shift-Invariant (LSI)** system, which behaves like a "black box" system. The key concepts of convolution, unit impulse function, and the properties of the Dirac delta function are discussed in detail.

### 1. Introduction to Linear Shift-Invariant (LSI) Systems
- An **LSI system** has two key properties:
  - **Linearity**: The output for a linear combination of inputs results in the same linear combination of outputs.
  - **Shift-Invariance**: Shifting the input by a certain amount results in a shifted output by the same amount.

- The system output, \( g(x) \), is defined as the **convolution** of the input signal \( f(x) \) and the system's **impulse response** \( h(x) \). This relationship is given by:
  - `g(x) = f(x) * h(x)`
  - Where `*` represents the convolution operation.
  
### 2. Problem: Finding the Impulse Response \( h(x) \)
- We are given that the system is convolving an unknown input with an unknown impulse response \( h(x) \). The challenge is to determine what \( h(x) \) is, given no explicit knowledge of the system.

### 3. Key Idea: Applying the Unit Impulse Function
- In order to find \( h(x) \), we apply a special input known as the **unit impulse function**, denoted as \( \delta(x) \).
  
- The **unit impulse function** \( \delta(x) \) has the following properties:
  - It is **infinitely thin** and **infinitely tall**.
  - Its width is \( 2 \epsilon \) and its height is \( \frac{1}{2 \epsilon} \).
  - Its area is always `1` as \( \epsilon \to 0 \), meaning it integrates to `1` across all space.
  
- Applying \( \delta(x) \) as the input to the LSI system gives us the system’s impulse response directly:
  - \( g(x) = \delta(x) * h(x) = h(x) \)
  
### 4. Conclusion: Impulse Response and Convolution
- By applying the **unit impulse function** \( \delta(x) \) as the input to the system, we can extract the impulse response \( h(x) \).
- This is because the convolution of any function with the **unit impulse** simply returns the function itself.

### 5. Summary of Key Equations:
- Convolution formula:
  - `g(x) = f(x) * h(x)`
  
- Impulse response when using the unit impulse function:
  - `g(x) = \delta(x) * h(x) = h(x)`
