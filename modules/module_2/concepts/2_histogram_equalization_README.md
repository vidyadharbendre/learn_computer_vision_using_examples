# Histogram Equalization: Step by Step

## Overview

This document explains **Histogram Equalization**, a technique in image processing used to improve the contrast of an image. The goal is to redistribute pixel intensities to enhance the clarity and detail in both bright and dark areas of an image.

---

## 5W1H: Histogram Equalization

### Who

**Who can use Histogram Equalization?**
- Image processing engineers
- Data scientists working with visual data
- Anyone who needs to improve the visibility of features in an image (e.g., medical imaging, satellite image processing, etc.)

---

### What

**What is Histogram Equalization?**

Histogram Equalization is a contrast enhancement technique that transforms the pixel intensity distribution of an image, making the intensity distribution more uniform. This allows for better visibility of image features.

The technique is particularly useful for:
- Enhancing poorly illuminated images
- Images where detail is hidden in the shadows or bright areas

**Key Components:**
1. **Histogram**: A graphical representation showing the distribution of pixel intensities.
2. **Cumulative Distribution Function (CDF)**: A cumulative sum of the histogram, used to map pixel intensities to new values.
3. **Equalized Image**: The resulting image after pixel intensities are redistributed.

---

### When

**When should you apply Histogram Equalization?**

Histogram Equalization is beneficial when:
- The image has low contrast (dark, overly bright, or washed out).
- You want to enhance image details that are not clearly visible.
- You need to preprocess an image for further tasks such as object detection or segmentation.

---

### Where

**Where is Histogram Equalization applied?**

Histogram Equalization is used in several domains, including:
- **Medical Imaging**: Enhancing details in X-rays, MRI scans, etc.
- **Satellite Imagery**: Improving the clarity of terrain and features.
- **Photography**: Enhancing underexposed or overexposed images.
- **Computer Vision Applications**: For preprocessing before feature extraction.

---

### Why

**Why use Histogram Equalization?**

Histogram Equalization helps to:
1. **Improve Visibility**: It makes previously hidden features visible by adjusting the intensity levels.
2. **Enhance Contrast**: It spreads out the pixel intensities more evenly, leading to better contrast.
3. **Better Image Interpretation**: Increases the readability of the image for both humans and machine learning models.

---

### How

**How does Histogram Equalization work?**

### Step-by-Step Process:

#### Step 1: Compute the Histogram
- A histogram represents the distribution of pixel intensity values in an image.
- For grayscale images, the histogram will have values from 0 (black) to 255 (white).

#### Step 2: Calculate the Cumulative Distribution Function (CDF)
- The CDF is a cumulative sum of the histogram values.
- This function tells us the relative percentile for each pixel intensity.

\[
\text{CDF}(I) = \sum_{i=0}^{I} \text{hist}(i)
\]

#### Step 3: Normalize the CDF
- Normalize the CDF so that it covers the entire intensity range (0 to 255 for 8-bit images).

\[
\text{CDF\_norm}(I) = \frac{\text{CDF}(I) - \text{CDF}_{\min}}{N - \text{CDF}_{\min}} \times 255
\]
Where:
- `CDF_min` is the smallest non-zero CDF value.
- `N` is the total number of pixels.

#### Step 4: Map the Original Intensities
- Use the normalized CDF to map the original pixel intensities to new values.

#### Step 5: Generate the Equalized Image
- Apply the new intensity values to the pixels, resulting in an equalized image where contrast is improved.

---

## Example Code: Histogram Equalization in Python

Here’s an example of how to implement histogram equalization in Python using OpenCV:

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the original image in grayscale
image = cv2.imread('path_to_your_image.jpg', 0)

# Apply Histogram Equalization
equalized_image = cv2.equalizeHist(image)

# Plot the original and equalized images
plt.figure(figsize=(10, 5))

# Original Image
plt.subplot(1, 2, 1)
plt.imshow(image, cmap='gray')
plt.title('Original Image')
plt.axis('off')

# Equalized Image
plt.subplot(1, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.show()
```