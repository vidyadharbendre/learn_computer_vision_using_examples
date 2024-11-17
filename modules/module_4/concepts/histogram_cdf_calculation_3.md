# Image Histogram and CDF Calculation

This README explains the step-by-step calculation of the **Histogram** and **Cumulative Distribution Function (CDF)** for an image. It includes comparisons between manual calculations using NumPy and OpenCV's built-in methods, with visualizations using Matplotlib.

---

## Histogram Calculation

The **Histogram** of an image represents the pixel intensity distribution. It shows the number of pixels corresponding to each intensity value (0-255).

### How the Histogram is Calculated

1. Using **NumPy**: Flatten the image and count the number of occurrences for each intensity value.
2. Using **OpenCV**: Use the `cv2.calcHist()` function.

---

## CDF (Cumulative Distribution Function) Calculation

The **CDF** is the cumulative sum of the histogram values. It provides the cumulative number of pixels at or below each intensity level.

### How the CDF is Calculated

1. Using **NumPy**: Compute the cumulative sum of the histogram values.
2. Using **OpenCV**: Use the cumulative sum of the histogram returned by `cv2.calcHist()`.

---

## Comparison: Manual Calculation (NumPy) vs OpenCV

Both methods yield the same results, but OpenCV's methods are optimized for image processing tasks.

---

## Code Example: Step-by-Step Demonstration

### 1. Load Image and Compute Histogram and CDF Manually (NumPy)

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Load the image in grayscale
image = cv2.imread('image.jpg', cv2.IMREAD_GRAYSCALE)

# Calculate histogram using NumPy
hist_np, bins = np.histogram(image.flatten(), bins=256, range=[0, 256])

# Calculate CDF manually using NumPy
cdf_np = hist_np.cumsum()

# Normalize the CDF
cdf_np_normalized = cdf_np * 255 / cdf_np[-1]

# Print histogram and CDF (NumPy)
print("Histogram (NumPy):", hist_np.tolist())
print("CDF (NumPy):", cdf_np.tolist())
print("Normalized CDF (NumPy):", cdf_np_normalized.tolist())
```

### 2. Compute Histogram and CDF Using OpenCV
```python
# Calculate histogram using OpenCV
hist_cv = cv2.calcHist([image], [0], None, [256], [0, 256]).flatten()

# Calculate CDF using OpenCV
cdf_cv = hist_cv.cumsum()

# Normalize the CDF
cdf_cv_normalized = cdf_cv * 255 / cdf_cv[-1]

# Print histogram and CDF (OpenCV)
print("Histogram (OpenCV):", hist_cv.tolist())
print("CDF (OpenCV):", cdf_cv.tolist())
print("Normalized CDF (OpenCV):", cdf_cv_normalized.tolist())
```

### 3. Visualize the Results

```python
# Plot the Histogram
plt.figure(figsize=(12, 6))
plt.subplot(1, 2, 1)
plt.title('Histogram')
plt.bar(range(256), hist_np, color='gray', label='NumPy')
plt.plot(hist_cv, color='red', linestyle='--', label='OpenCV')
plt.legend()
plt.xlabel('Intensity')
plt.ylabel('Pixel Count')

# Plot the CDF
plt.subplot(1, 2, 2)
plt.title('Cumulative Distribution Function (CDF)')
plt.plot(cdf_np, label='NumPy CDF', color='blue')
plt.plot(cdf_cv, label='OpenCV CDF', color='green', linestyle='--')
plt.legend()
plt.xlabel('Intensity')
plt.ylabel('Cumulative Pixel Count')

plt.tight_layout()
plt.show()

```
