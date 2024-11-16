# Image Histogram and CDF Calculation

This README explains the step-by-step calculation of the **Histogram** and **Cumulative Distribution Function (CDF)** for an image, using the provided values.

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

| Intensity | CDF Value |
|-----------|-----------|
| 0         | 0         |
| 32        | 11        |
| 64        | 8589      |
| 96        | 10098     |
| 128       | 14908     |
| 160       | 21689     |
| 192       | 28079     |
| 224       | 29561     |

### How CDF is Calculated

To calculate the CDF, we start from intensity level 0 and sum the pixel counts up to each intensity level. For example:

1. **Intensity 0**: The CDF value is simply the histogram value for intensity 0, which is `0`.
2. **Intensity 32**: The CDF value is the sum of all previous histogram values and the current histogram value: `0 + 7 = 7`.
3. **Intensity 64**: The CDF value is the sum of all previous values plus the histogram value at intensity 64: `7 + 83 = 90`.
4. **Intensity 96**: The CDF value is: `90 + 61 = 151`, and so on.

### Normalization of CDF

In some cases, the CDF is normalized to fit a specific range, such as from 0 to 255. This can be done as follows:

1. Compute the CDF as shown above.
2. Normalize the CDF by dividing each value by the total number of pixels in the image, and then multiply by 255.

For example:
Normalized CDF = CDF(i) / Total Pixels * 255


---

## Explanation of the CDF Scaling

The CDF values provided in the example might be scaled or normalized. The original image CDF values may look like:

| Intensity | CDF Value |
|-----------|-----------|
| 0         | 0         |
| 32        | 11        |
| 64        | 8589      |
| 96        | 10098     |
| 128       | 14908     |
| 160       | 21689     |
| 192       | 28079     |
| 224       | 29561     |

This suggests that the CDF has been scaled or normalized to fit a particular range, possibly to the range of pixel values in an image.

---

## Conclusion

- The **Histogram** represents the distribution of pixel intensities in the image.
- The **CDF** is the cumulative sum of histogram values and helps in understanding the cumulative distribution of pixel intensities.
- In some cases, the **CDF** is normalized to a specific range (like 0 to 255) for further processing, such as **histogram equalization**.

---

## Example Code

Here is an example code snippet to compute the histogram and CDF for an image:

```python
import numpy as np
import cv2

# Load the image (convert to grayscale if necessary)
image = cv2.imread('image.jpg', cv2.IMREAD_GRAYSCALE)

# Calculate the histogram
histogram = cv2.calcHist([image], [0], None, [256], [0, 256])

# Calculate the CDF
cdf = histogram.cumsum()

# Normalize the CDF to the range 0-255
cdf_normalized = cdf * 255 / cdf[-1]

print("Histogram Values:", histogram)
print("CDF Values:", cdf_normalized)

