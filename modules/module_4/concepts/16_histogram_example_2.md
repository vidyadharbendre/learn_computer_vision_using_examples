# Image Histogram and CDF Calculation

This README explains the step-by-step calculation of the **Histogram** and **Cumulative Distribution Function (CDF)** for an image, using the provided values.

---

## Histogram Calculation

The **Histogram** of an image is a representation of the pixel intensity distribution. It shows how many pixels in the image correspond to each intensity value, ranging from 0 to 255.

### Histogram Values for Original Image

| Intensity | Pixel Count |
|-----------|-------------|
| 0         | 0           |
| 32        | 7           |
| 64        | 83          |
| 96        | 61          |
| 128       | 210         |
| 160       | 194         |
| 192       | 135         |
| 224       | 24          |

The histogram above shows the count of pixels for each intensity level.

### How the Histogram is Calculated

To calculate the histogram, we simply count the number of pixels in the image that correspond to each intensity level. For example:
- **Intensity 0**: There are 0 pixels with intensity 0.
- **Intensity 32**: There are 7 pixels with intensity 32, and so on.

---

## CDF (Cumulative Distribution Function) Calculation

The **CDF** is the cumulative sum of the histogram values. It helps in understanding the cumulative number of pixels at or below each intensity level.

### CDF Values for Original Image

| Intensity | CDF Value (Sum of Pixels) |
|-----------|---------------------------|
| 0         | 0                         |
| 32        | 7                         |
| 64        | 90                        |
| 96        | 151                       |
| 128       | 361                       |
| 160       | 555                       |
| 192       | 690                       |
| 224       | 714                       |

### How the CDF is Calculated

To calculate the CDF, we start from intensity level 0 and sum the pixel counts up to each intensity level. For example:
1. **Intensity 0**: The CDF value is the histogram value at intensity 0, which is `0`.
2. **Intensity 32**: The CDF value is the sum of all previous histogram values and the current histogram value: `0 + 7 = 7`.
3. **Intensity 64**: The CDF value is: `7 + 83 = 90`.
4. **Intensity 96**: The CDF value is: `90 + 61 = 151`.
5. And so on, until the final intensity.

---

### Normalization of CDF

The **Normalized CDF** scales the values to a specific range, such as `0` to `255`, using the formula:

`Normalized CDF = (CDF Value / Total Number of Pixels) * 255`

#### Example for Intensity 32:
1. **CDF Value at Intensity 32**: `7`.
2. **Total Number of Pixels**: `714` (sum of all histogram values).
3. Normalize the CDF:
   `Normalized CDF = (7 / 714) * 255 = 2.5`
4. Approximation: `2.5` is the scaled value, though rounding may occur for visualization.

---

## Final CDF Values (Normalized to 0-255)

| Intensity | Normalized CDF |
|-----------|----------------|
| 0         | 0              |
| 32        | 2.5            |
| 64        | 32.1           |
| 96        | 53.9           |
| 128       | 128.8          |
| 160       | 198.2          |
| 192       | 246.3          |
| 224       | 255.0          |

---

## Conclusion

- The **Histogram** represents the pixel intensity distribution of the image.
- The **CDF** represents the cumulative pixel count up to each intensity.
- The **Normalized CDF** scales the CDF to a specified range, such as `0` to `255`, useful for applications like histogram equalization.

---

## Example Code

Here is an example code snippet to compute the histogram and CDF for an image:

```python
import numpy as np
import cv2

# Load the image (convert to grayscale if necessary)
image = cv2.imread('image.jpg', cv2.IMREAD_GRAYSCALE)

# Calculate the histogram
histogram, _ = np.histogram(image.flatten(), bins=256, range=[0, 256])

# Calculate the CDF
cdf = histogram.cumsum()

# Normalize the CDF to the range 0-255
cdf_normalized = cdf * 255 / cdf[-1]

print("Histogram Values:", histogram.tolist())
print("CDF Values:", cdf.tolist())
print("Normalized CDF Values:", cdf_normalized.tolist())
```