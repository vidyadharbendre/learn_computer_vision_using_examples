# Image Processing Concepts

## 1. Image as a Function of f(x, y)
An image can be represented as a 2D function, where the intensity of light at any given point `(x, y)` is expressed as `f(x, y)`. If we are dealing with a **color image**, we have multiple channels (Red, Green, and Blue). These channels are represented as:
- `r(x, y)` - Red channel
- `g(x, y)` - Green channel
- `b(x, y)` - Blue channel

Thus, the color image can be described as a combination of these three functions:
- `r(x, y)`, `g(x, y)`, `b(x, y)`.

Each function corresponds to a particular intensity value for its respective color channel at a specific `(x, y)` location.

## 2. Pixel Transformation (Point Processing)

### Definition
Pixel (point) processing is the simplest form of image transformation, where each pixel in the image is transformed based on its current intensity or color value, **independent of its position in the image**.

The pixel transformation is represented as a function `T` that takes the intensity value `f(x, y)` of a pixel and maps it to a new intensity value `g(x, y)`:
- `g(x, y) = T[f(x, y)]`

### Brightness Mapping
One common application of point processing is **brightness adjustment**. Here, the intensity of every pixel is modified by a constant value `C` to brighten or darken the image:
- `g(x, y) = f(x, y) + C`

### Color Transformation
Similarly, color transformations involve mapping one color value to another. For instance, adjusting the Red, Green, or Blue channels in a color image:
- `r'(x, y) = T[r(x, y)]`
- `g'(x, y) = T[g(x, y)]`
- `b'(x, y) = T[b(x, y)]`

### Types of Pixel Transformations
- **Linear transformations**: These involve scaling the pixel values linearly, such as multiplying the intensity by a factor to increase or decrease brightness.
- **Non-linear transformations**: These include operations like **gamma correction**, **thresholding**, or **logarithmic transformations**. Non-linear mappings are often used for contrast enhancement or tone adjustments.

### Examples:
- **Brightness Scaling**: If we multiply every pixel’s brightness by a factor of `A`, we can brighten or darken the image:
  - `g(x, y) = A * f(x, y)`

- **Gamma Correction**: To adjust for non-linearity in display devices, the following gamma correction is applied:
  - `g(x, y) = f(x, y) ^ (1 / γ)`

### Key Point:
In pixel (point) processing, the transformation of each pixel depends **only on its value** and does not take into account neighboring pixels. This makes it computationally simple, but it may not be sufficient for advanced image processing tasks.

## 3. Color Mapping
In the case of color images, the RGB values are transformed individually using the same transformation function or different functions for each channel. Color balance, saturation, and other color manipulations are done by modifying the mappings of the RGB channels.

---

### Summary
This section has covered basic pixel (point) transformations, which involve mapping a pixel's brightness or color to another value. These operations are fundamental in many image processing applications like brightness adjustment, contrast enhancement, and color correction.

Pixel transformations allow us to process the image **independently** of its spatial information, making them ideal for basic enhancements or corrections to the image's appearance.

---

Feel free to experiment with various transformations to observe their effect on an image's brightness, contrast, and colors!
