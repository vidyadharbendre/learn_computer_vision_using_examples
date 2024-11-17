# Color Image Smoothing and Sharpening

This repository demonstrates grayscale and color image smoothing using spatial filtering operations. It includes Python code examples to perform image smoothing on both grayscale and color images. The repository also illustrates how to work with RGB and HSI models for image processing.

## Background

### Grayscale Image Smoothing

Grayscale image smoothing can be viewed as a spatial filtering operation where the coefficients of the filtering kernel are uniform. The smoothing process involves replacing each pixel with the average of its neighboring pixels in the kernel's neighborhood. This is typically done using a kernel with the same values.

Mathematically, the smoothing operation for a grayscale image is defined as:
g(x, y) = (1/K) * sum(f(s, t)) for (s, t) ∈ S_xy

Where:
- `g(x, y)` is the new smoothed pixel value at position (x, y).
- `S_xy` is the neighborhood of the pixel (x, y).
- `K` is the total number of pixels in the neighborhood.

### Color Image Smoothing

For color images (in RGB format), the concept of smoothing can be extended. Instead of processing scalar intensity values, we deal with RGB component vectors.

The operation for color image smoothing is performed independently for each color plane (R, G, B). The formula for this smoothing operation is:

c(x, y) = (1/K) * sum(c(s, t)) for (s, t) ∈ S_xy

Where `c(x, y)` represents the RGB vector of the pixel at (x, y).

This approach smooths each color component independently and then reconstructs the full-color image.

### HSI Model for Smoothing

The HSI (Hue, Saturation, Intensity) color model separates intensity from color information. This model allows for more flexible smoothing:
- By smoothing only the intensity component, you can preserve the hue and saturation of the image, keeping the color intact while modifying the brightness.

### Example 6.12: Color Image Smoothing

Consider an example where we smooth the RGB image using a 5x5 averaging kernel. The individual components of the RGB image are processed independently, as shown in the example.

## Python Code Implementation

The following sections show how the smoothing operations are implemented using Python and OpenCV.

### Grayscale Smoothing using OpenCV

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load image in grayscale
image = cv2.imread('image.jpg', cv2.IMREAD_GRAYSCALE)

# Define kernel size for smoothing
kernel_size = 5
kernel = np.ones((kernel_size, kernel_size), np.float32) / (kernel_size * kernel_size)

# Apply smoothing filter to the image
smoothed_image = cv2.filter2D(image, -1, kernel)

# Display original and smoothed images
plt.figure(figsize=(10, 5))
plt.subplot(1, 2, 1)
plt.imshow(image, cmap='gray')
plt.title('Original Grayscale Image')
plt.subplot(1, 2, 2)
plt.imshow(smoothed_image, cmap='gray')
plt.title('Smoothed Grayscale Image')
plt.show()
```
### Color Image Smoothing using OpenCV
```python
# Load image in color (RGB)
image = cv2.imread('image.jpg')

# Define kernel size for smoothing
kernel_size = 5
kernel = np.ones((kernel_size, kernel_size), np.float32) / (kernel_size * kernel_size)

# Split the image into RGB channels
B, G, R = cv2.split(image)

# Apply smoothing to each channel independently
smoothed_R = cv2.filter2D(R, -1, kernel)
smoothed_G = cv2.filter2D(G, -1, kernel)
smoothed_B = cv2.filter2D(B, -1, kernel)

# Merge the smoothed channels back together
smoothed_image = cv2.merge([smoothed_B, smoothed_G, smoothed_R])

# Display the original and smoothed color images
plt.figure(figsize=(10, 5))
plt.subplot(1, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.subplot(1, 2, 2)
plt.imshow(cv2.cvtColor(smoothed_image, cv2.COLOR_BGR2RGB))
plt.title('Smoothed Color Image')
plt.show()
```

### Intensity Component Smoothing using HSI Model

In this example, we smooth only the intensity component while leaving the hue and saturation components unchanged.

```python
# Convert image to HSI
hsv_image = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)

# Extract the intensity channel (I) and apply smoothing
h, s, i = cv2.split(hsv_image)
smoothed_i = cv2.filter2D(i, -1, kernel)

# Merge the smoothed intensity channel back with hue and saturation
smoothed_hsv_image = cv2.merge([h, s, smoothed_i])

# Convert back to RGB for visualization
smoothed_rgb_image = cv2.cvtColor(smoothed_hsv_image, cv2.COLOR_HSV2BGR)

# Display the result
plt.figure(figsize=(10, 5))
plt.imshow(cv2.cvtColor(smoothed_rgb_image, cv2.COLOR_BGR2RGB))
plt.title('Smoothed Image with Intensity Smoothing Only')
plt.show()
```

### Conclusion
This repository demonstrates basic and advanced image smoothing techniques, both for grayscale and color images. By exploring both the RGB and HSI color models, we can perform sophisticated image processing operations such as preserving color information while modifying image brightness or sharpness.

