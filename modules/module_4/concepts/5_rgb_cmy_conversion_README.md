# RGB to CMY and CMY to RGB Conversion

## Overview
This document explains the process of converting images between the **RGB (Red, Green, Blue)** and **CMY (Cyan, Magenta, Yellow)** color spaces. 

---

## 1. Who Needs This?
This guide is intended for:
- **Developers and Data Scientists**: Working on image processing tasks requiring color space conversions.
- **Graphic Designers**: Understanding how colors are represented in printing versus digital formats.
- **Educators and Students**: Learning or teaching image processing concepts.
- **Anyone Curious**: About how RGB and CMY color spaces relate.

---

## 2. What Is This About?
This is about understanding and implementing:
- **RGB to CMY Conversion**: Used in printing, where colors are represented as subtractive color components.
- **CMY to RGB Conversion**: Reconstructing the original colors from subtractive components for digital displays.

Key formulas:
- **RGB to CMY**: \( \text{CMY} = 1 - \text{RGB (normalized)} \)
- **CMY to RGB**: \( \text{RGB} = 1 - \text{CMY} \)

### Example:
For an RGB pixel \([255, 128, 64]\):
- Normalized RGB: \([1.0, 0.502, 0.251]\)
- CMY: \([0.0, 0.498, 0.749]\)
- Reconstructed RGB: \([255, 128, 64]\)

---

## 3. When Is This Useful?
- **Image Editing**: Transforming images to CMY for professional color printing.
- **Data Visualization**: Representing images in alternative color spaces.
- **Machine Learning**: Preprocessing images to study effects of subtractive color spaces on model performance.
- **Teaching and Research**: Demonstrating the interplay between additive and subtractive color models.

---

## 4. Where Can It Be Applied?
- **Digital Platforms**: Any RGB-based image source like cameras, computer screens, or digital art.
- **Printing**: Converting digital images to CMY for printers, where subtractive colors are used.
- **Real-Time Systems**: Using OpenCV or similar libraries to perform on-the-fly conversions in applications like augmented reality.

---

## 5. Why Does This Matter?
Understanding these conversions:
- **Bridges the Gap**: Between additive (RGB) and subtractive (CMY) color models.
- **Enables Cross-Media Compatibility**: Ensures images look as intended across digital and print media.
- **Improves Color Manipulation**: Gives more control over color transformations.

---

## 6. How To Implement It?
### Code Example in Python
```python
import os
import cv2
import numpy as np
import matplotlib.pyplot as plt

def rgb_to_cmy(image):
    """
    Converts an RGB image to CMY color space.
    """
    normalized_rgb = image / 255.0
    cmy_image = 1 - normalized_rgb
    return cmy_image

def cmy_to_rgb(cmy_image):
    """
    Converts a CMY image back to RGB color space.
    """
    rgb_image = 1 - cmy_image
    return (rgb_image * 255).astype(np.uint8)

# Load the image
image_path = os.path.join(os.getcwd(), 'data', 'images', 'example.jpg')
rgb_image = cv2.imread(image_path)
rgb_image = cv2.cvtColor(rgb_image, cv2.COLOR_BGR2RGB)

# Convert RGB to CMY
cmy_image = rgb_to_cmy(rgb_image)

# Convert CMY back to RGB
reconstructed_rgb = cmy_to_rgb(cmy_image)

# Display images
plt.figure(figsize=(12, 8))
plt.subplot(1, 3, 1)
plt.imshow(rgb_image)
plt.title("Original RGB Image")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(1 - cmy_image)  # Invert CMY for viewing
plt.title("CMY Image (Inverted for View)")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(reconstructed_rgb)
plt.title("Reconstructed RGB Image")
plt.axis("off")

plt.tight_layout()
plt.show()
```
