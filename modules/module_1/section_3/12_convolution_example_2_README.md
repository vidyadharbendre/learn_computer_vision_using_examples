# Convolution of Rectangular and Triangular Functions

This document provides a detailed explanation of the convolution of a rectangular function and a triangular function, highlighting its properties and resulting shape.

## Introduction

Convolution is a fundamental operation in signal processing that describes how two signals interact. In this case, we will convolve a rectangular function 'f(x)' with a triangular function 'h(x)'.

## Functions Definition

1. **Rectangular Function 'f(x)'**:
   - Defined as:
     ```
     f(x) = {
       1,  for -1 ≤ x ≤ 1
       0,  otherwise
     }
     ```

2. **Triangular Function 'h(x)'**:
   - Defined as:
     ```
     h(x) = {
       1 - |x|,  for -1 ≤ x ≤ 1
       0,  otherwise
     }
     ```

## Visual Explanation of the Convolution

### Step-by-Step Process

1. **Function Definitions**:
   - 'f(x)' is a rectangle ranging from \(-1\) to \(1\) with a height of \(1\).
   - 'h(x)' is a triangle ranging from \(-1\) to \(1\) with a peak at \(0\) having a height of \(1\).

2. **Convolution Calculation**:
   - The convolution \( g(x) \) is defined as:
     ```
     g(x) = ∫_{-∞}^{∞} f(τ) h(x - τ) dτ
     ```

3. **Output Characteristics**:
   - The resulting convolution 'g(x)' will resemble a parabolic shape (or a normal curve) ranging from \(-2\) to \(2\), with a peak height of \(1\) at \(x = 0\).
   - For 'x < -2' or 'x > 2', the output 'g(x) = 0' since there is no overlap between 'f(τ)' and 'h(x - τ)'.
   - For '\(-2 < x < -1\)' and '\(1 < x < 2\)', the convolution output is triangular, representing partial overlap between the two functions.
   - For '\(-1 ≤ x ≤ 1\)', where the rectangular function and triangular function fully overlap, the convolution output forms a smooth curve resembling a parabola.

## Conclusion

The convolution of a rectangular function 'f(x)' and a triangular function 'h(x)' illustrates the fundamental principles of signal processing. The resulting output 'g(x)' demonstrates how the shapes interact, creating a smooth transition from the overlapping functions.

### Visualization

A graph illustrating these functions and their convolution can greatly enhance understanding. 

![Convolution of Rectangular and Triangular Functions](link_to_your_image)

---

This README serves as a comprehensive guide to understanding the convolution process for these specific functions.
