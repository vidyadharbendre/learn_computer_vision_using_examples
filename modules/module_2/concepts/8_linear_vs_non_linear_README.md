# Image Processing: Linear vs Non-Linear Filters

This project demonstrates the concepts of **linear** and **non-linear** filters in image processing, using point, local, and global operations. It provides a simple Python example to illustrate the key differences between the two types of filters and how they relate to common image operations.

## Table of Contents
1. [Introduction](#introduction)
2. [Types of Image Operations](#types-of-image-operations)
   - [Point Operations](#point-operations)
   - [Local Operations](#local-operations)
   - [Global Operations](#global-operations)
3. [Linear Filters](#linear-filters)
4. [Non-Linear Filters](#non-linear-filters)
5. [Python Examples](#python-examples)
   - [Linear Filter Example](#linear-filter-example)
   - [Non-Linear Filter Example](#non-linear-filter-example)
6. [Conclusion](#conclusion)

## Introduction
In image processing, filters are used to modify or enhance images. Filters can be categorized into two types: **linear** and **non-linear**. These filters are applied to pixels based on different operations—point, local, or global—each affecting the image in different ways.

### Key Concepts
- **Linear Filter**: Applies a linear transformation to the pixel values (e.g., convolution with a kernel).
- **Non-Linear Filter**: Applies non-linear operations like median filtering, which selects a value based on specific criteria.

## Types of Image Operations

### Point Operations
- **Definition**: Point operations modify each pixel independently based only on its own value.
- **Linear Example**: Adjusting brightness by adding a constant to each pixel value.
- **Non-Linear Example**: Gamma correction, where pixel values are transformed based on a power-law function.

### Local Operations
- **Definition**: Local operations modify each pixel based on its neighboring pixels within a specified window or kernel.
- **Linear Example**: Gaussian blur, where a weighted average is computed from neighboring pixels.
- **Non-Linear Example**: Median filter, which replaces each pixel with the median value of its neighboring pixels, reducing noise like salt-and-pepper noise.

### Global Operations
- **Definition**: Global operations use all pixels in the image to compute the new value for each pixel.
- **Linear Example**: Fourier transform, which processes the entire image in the frequency domain.
- **Non-Linear Example**: Histogram equalization, where pixel intensities are redistributed to improve contrast.

## Linear Filters
A **linear filter** modifies the image by applying a linear combination of the pixel values. The most common linear filter operation is **convolution**, where a kernel is applied to the image to smooth, sharpen, or detect edges.

### Equation (Linear Filter):
\[
g(x, y) = \sum_{i=-k}^{k} \sum_{j=-k}^{k} h(i, j) \cdot f(x - i, y - j)
\]
Where:
- \( g(x, y) \) is the output pixel value.
- \( f(x, y) \) is the original pixel value.
- \( h(i, j) \) is the kernel applied to the image.
  
Common linear filters include **mean filtering**, **Gaussian blur**, and **sharpening**.

## Non-Linear Filters
A **non-linear filter** uses a non-linear operation to modify the pixel values. The most common example is the **median filter**, which replaces each pixel with the median value of its neighborhood. This filter is particularly useful for reducing impulse noise.

### Equation (Non-Linear Filter):
\[
g(x, y) = \text{median}\left( \{ f(x - i, y - j) \,|\, (i, j) \in \text{neighborhood} \} \right)
\]
Where:
- \( g(x, y) \) is the output pixel value.
- \( f(x, y) \) is the original pixel value.
- The median function selects the middle value from the sorted set of neighboring pixels.

## Python Examples

### Linear Filter Example
The following example applies a **mean filter** to an image, a typical linear filter.

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load image
image = cv2.imread('image.jpg', cv2.IMREAD_GRAYSCALE)

# Apply linear filter (mean filter)
kernel = np.ones((3, 3), np.float32) / 9
linear_filtered_image = cv2.filter2D(image, -1, kernel)

# Display
plt.imshow(linear_filtered_image, cmap='gray')
plt.title("Linear Filter (Mean Filter)")
plt.show()
```

### Non-Linear Filter Example
The following example applies a median filter to an image, which is a non-linear filter.

```python
import cv2
import matplotlib.pyplot as plt

# Load image
image = cv2.imread('image.jpg', cv2.IMREAD_GRAYSCALE)

# Apply non-linear filter (median filter)
non_linear_filtered_image = cv2.medianBlur(image, 3)

# Display
plt.imshow(non_linear_filtered_image, cmap='gray')
plt.title("Non-Linear Filter (Median Filter)")
plt.show()

```

## Conclusion
Linear and non-linear filters are fundamental in image processing, each suitable for different types of tasks. Linear filters, like convolution with kernels, are widely used for smoothing and sharpening images. Non-linear filters, like the median filter, are excellent for reducing noise while preserving edges.

Understanding how to apply these filters and when to use them can greatly improve your ability to process and enhance images effectively.