# Image Sharpening using the Laplacian Operator

This project demonstrates **image sharpening** techniques using the **Laplacian operator** applied in two different approaches:
- **RGB-based sharpening**
- **HSI-based sharpening**

## Overview

The goal is to sharpen the image by emphasizing high-frequency details, such as edges, using the Laplacian operator. This operator computes the second derivative of the image, highlighting rapid changes in intensity (edges and noise). We apply this operator in two different ways to observe and compare the results:
1. Sharpening each **RGB channel** separately.
2. Sharpening only the **Intensity (I) channel** in the **HSI color space**.

### Expected Output
- **Original Image (RGB):** The unprocessed image before any sharpening is applied.
- **Sharpened Image (RGB):** The sharpened image achieved by applying the Laplacian to individual RGB components.
- **Sharpened Image (HSI):** The sharpened image based on the HSI model, where only the intensity channel is sharpened.
- **Difference Image (RGB - HSI):** Highlights the discrepancies between the RGB-based and HSI-based sharpening methods.

## Implementation Steps

### 1. Sharpen the RGB Image:
- Apply the Laplacian operator to each channel (R, G, B) separately.
- Combine the sharpened channels to reconstruct the sharpened RGB image.

### 2. Sharpen the Intensity Component in HSI:
- Convert the image to the HSI color space.
- Apply the Laplacian operator to the Intensity (I) channel.
- Reconstruct the sharpened HSI image by combining the sharpened intensity with the original hue and saturation.
- Convert the result back to the RGB color space.

### 3. Compare the Results:
- Highlight the differences between the RGB-based and HSI-based sharpening to observe the impact of sharpening only the intensity channel in the HSI model.

## Code Implementation

```python
import os
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Function to display images for comparison
def display_images_sharpening(original, sharpened_rgb, sharpened_hsi, diff_image,
                              title_original, title_sharpened_rgb, title_sharpened_hsi, title_diff):
    plt.figure(figsize=(16, 8))

    plt.subplot(2, 2, 1)
    plt.imshow(cv2.cvtColor(original, cv2.COLOR_BGR2RGB))
    plt.title(title_original)
    plt.axis('off')

    plt.subplot(2, 2, 2)
    plt.imshow(cv2.cvtColor(sharpened_rgb, cv2.COLOR_BGR2RGB))
    plt.title(title_sharpened_rgb)
    plt.axis('off')

    plt.subplot(2, 2, 3)
    plt.imshow(cv2.cvtColor(sharpened_hsi, cv2.COLOR_BGR2RGB))
    plt.title(title_sharpened_hsi)
    plt.axis('off')

    plt.subplot(2, 2, 4)
    plt.imshow(diff_image, cmap='gray')
    plt.title(title_diff)
    plt.axis('off')

    plt.tight_layout()
    plt.show()


# Define Laplacian kernel
laplacian_kernel = np.array([[0, -1, 0],
                             [-1, 4, -1],
                             [0, -1, 0]], dtype=np.float32)

# Load the image
image_path = os.path.join(os.getcwd(), 'data', 'images', 'lena_color.jpg')
#image_path = os.path.join(os.getcwd(), 'data', 'images', 'roses.jpg')  # Replace with your image path
#image_path = os.path.join(os.getcwd(), 'data', 'images', 'worldview-1.jpg') 
image = cv2.imread(image_path)  # Load the image in BGR format


# ------------ RGB-Based Sharpening ------------ #
# Split RGB channels
R, G, B = cv2.split(image)

# Apply Laplacian to each channel
laplacian_R = cv2.filter2D(R, -1, laplacian_kernel)
laplacian_G = cv2.filter2D(G, -1, laplacian_kernel)
laplacian_B = cv2.filter2D(B, -1, laplacian_kernel)

# Combine the Laplacians
sharpened_rgb = cv2.merge([R + laplacian_R, G + laplacian_G, B + laplacian_B])

# ------------ HSI-Based Sharpening ------------ #
# Convert to HSI (use HSV as a proxy for HSI in OpenCV)
image_hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
H, S, I = cv2.split(image_hsv)

# Apply Laplacian to the Intensity channel
laplacian_I = cv2.filter2D(I, -1, laplacian_kernel)

# Combine the sharpened intensity with original H and S channels
sharpened_hsv = cv2.merge([H, S, I + laplacian_I])
sharpened_hsi = cv2.cvtColor(sharpened_hsv, cv2.COLOR_HSV2BGR)

# ------------ Compute Difference ------------ #
diff_image = cv2.absdiff(sharpened_rgb, sharpened_hsi)

# ------------ Display Results ------------ #
display_images_sharpening(
    original=image,
    sharpened_rgb=sharpened_rgb,
    sharpened_hsi=sharpened_hsi,
    diff_image=diff_image,
    title_original="Original Image (RGB)",
    title_sharpened_rgb="Sharpened Image (RGB Components)",
    title_sharpened_hsi="Sharpened Image (HSI Intensity Component)",
    title_diff="Difference Image (RGB - HSI)"
)
```
