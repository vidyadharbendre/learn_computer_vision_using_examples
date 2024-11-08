# Edge Detection Techniques

## Overview
This document explains edge detection techniques in image processing, focusing on first and second derivative-based approaches to identify edges.

---

## Table of Contents
1. [Introduction to Edge Detection](#introduction-to-edge-detection)
2. [Gradient and First Derivative](#gradient-and-first-derivative)
3. [Second Derivative and Zero Crossing](#second-derivative-and-zero-crossing)
4. [Common Edge Detection Filters](#common-edge-detection-filters)
   - Sobel Filter
   - Prewitt Filter
   - Laplacian of Gaussian (LoG)
5. [References](#references)

---

## Introduction to Edge Detection
Edge detection is a fundamental tool in image processing used to identify significant changes in intensity, marking object boundaries and structural details. By analyzing pixel intensity variations, we can apply filters based on derivatives to detect edges.

---

## Gradient and First Derivative
Gradients are effective estimators of edges because they measure the rate of change in intensity. The **first derivative** of an image represents how quickly pixel values change, with high gradient values indicating edges.

- **First Derivative of Gaussian**: This approach smooths an image using a Gaussian filter and then applies the gradient, detecting edges where the gradient magnitude is high.

For example, the gradient can be computed using filters such as:
- **Prewitt Filter** in the x-direction:
