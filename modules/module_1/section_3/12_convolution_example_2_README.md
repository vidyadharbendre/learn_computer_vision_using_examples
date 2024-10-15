# Convolution of a Rectangular and Triangular Function

## Problem Setup

In this example, we convolve a rectangular function 'f(x)' with a triangular function 'h(x)'. The rectangular function is a step function ranging from -1 to 1, and the triangular function also ranges from -1 to 1 with a peak at 0. The goal is to understand the output of this convolution step by step.

### Functions
1. **Rectangular Function 'f(x)'**:
   - 'f(x)' is defined as:
   - 'f(x) = 1, -1 ≤ x ≤ 1'
   - 'f(x) = 0, \text{otherwise}'

2. **Triangular Function 'h(x)'**:
   - 'h(x)' is defined as:
   - 'h(x) = 1 - |x|, -1 ≤ x ≤ 1'
   - 'h(x) = 0, \text{otherwise}'

## Convolution Process

The convolution of two functions 'f(x)' and 'h(x)' is represented as:

'**g(x) = ∫_{-∞}^{∞} f(τ) h(x - τ) dτ**'

### Step-by-Step Convolution

1. **Flipping the Triangular Function 'h(x)'**:
   - Since 'h(x)' is symmetric around x = 0, flipping 'h(τ)' does not change its shape. Therefore, 'h(-τ)' looks the same as 'h(τ)'.
   - The flipped function remains a triangle from -1 to 1, with the peak at 0.

2. **Shifting 'h(τ)'**:
   - Shift the flipped triangular function 'h(τ)' by 'x'. The function becomes 'h(x - τ)'.
   - This shift slides the triangle left or right along the 'x' axis.

3. **Overlaying and Product Calculation**:
   - For each shift 'x', overlay the shifted triangular function 'h(x - τ)' on top of the rectangular function 'f(τ)'.
   - Take the product 'f(τ) * h(x - τ)' at each point. For values of 'τ' outside [-1, 1], the rectangular function is 0, so the product is 0.
   
4. **Summation (Integration)**:
   - Sum the product values over the entire range of 'τ'. This integral yields the output of the convolution at each point 'x'.
   - Mathematically, this is represented as:
   - '**g(x) = ∫_{-1}^{1} f(τ) * h(x - τ) dτ**'

## Output: The Convolved Signal

The result 'g(x)' is the convolution of the rectangular and triangular functions:

- For 'x < -2' or 'x > 2', the output 'g(x) = 0' since there is no overlap between 'f(τ)' and 'h(x - τ)'.
- For '-2 < x < -1' and '1 < x < 2', the convolution output is a triangular shape, which is the partial overlap between the two functions.
- For '-1 ≤ x ≤ 1', where the rectangular function and triangular function fully overlap, the convolution output is a trapezoid.

## Visual Explanation of Convolution

1. Flip 'h(x)', which is the triangular function.
2. Shift it along 'x' to form 'h(x - τ)'.
3. Multiply the shifted triangular function by the rectangular function.
4. Integrate the result to obtain a single number at each 'x', forming the output function 'g(x)'.

The entire process results in a smoothed, trapezoidal output signal due to the convolution of the sharp edges of the rectangular function and the gradual changes of the triangular function.

## Conclusion

This process demonstrates how convolution with a triangular function smooths the output signal. The convolution operation is vital in signal processing as it combines the characteristics of two functions, which in this case transforms a rectangular input signal into a trapezoidal output.
