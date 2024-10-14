# Image as a Function of Pixel Coordinates

## Introduction
In digital image processing, an image can be viewed as a two-dimensional function of intensity values. Each point in the image corresponds to a specific pixel, and its value represents the brightness or color intensity.

## 1. Image as a Function
An image can be represented as a function:
- Let us consider an image as a function of coordinates **f(x, y)**.
  - Here, **x** and **y** are the spatial coordinates (representing the horizontal and vertical axes).
  - **f(x, y)** represents the intensity value at a specific point (x, y) in the image.
  
  For grayscale images, this intensity value is usually a single number that denotes the brightness at each pixel.

### Formula:
- Grayscale Image: 
  - The intensity value at a point can be denoted as `'f(x, y)'`, where **x** and **y** are pixel coordinates and **f** gives the intensity.

## 2. Color Image as Multiple Functions
For color images, there are typically three color channels: **Red (R)**, **Green (G)**, and **Blue (B)**. Each channel represents the intensity of a color at a specific point in the image.

- For color images, we can represent the image as multiple functions:
  - **R(x, y)**: Red channel intensity at position (x, y)
  - **G(x, y)**: Green channel intensity at position (x, y)
  - **B(x, y)**: Blue channel intensity at position (x, y)

Each channel's value corresponds to the color intensity at that particular pixel position. Combining these channels allows us to represent the full color image.

### Formula:
- Color Image:
  - The color value at a pixel can be represented as a combination of three functions:
    - `R(x, y)`: Red intensity function at (x, y)
    - `G(x, y)`: Green intensity function at (x, y)
    - `B(x, y)`: Blue intensity function at (x, y)

## Conclusion
Understanding an image as a function of its pixel coordinates helps break down how we perceive grayscale and color images. In the case of color images, each pixel is defined by three distinct intensity values corresponding to red, green, and blue components, all of which together form the final color at that pixel.

This functional representation is fundamental in image processing, laying the groundwork for more advanced operations such as filtering, transformations, and color space conversions.
