# Histogram Equalization - CDF Calculation and Equalization

## Introduction

Histogram Equalization is a technique used in image processing to enhance the contrast of an image. This is done by transforming the intensity values of the pixels so that they span the entire intensity range. The technique uses the **Cumulative Distribution Function (CDF)** of pixel intensities to remap the image's pixel values.

In this example, we will calculate the **CDF**, **Normalized CDF**, and apply the histogram equalization using the calculated CDF values.

---

## Steps to Calculate CDF, Normalized CDF, and Equalized CDF

### 1. **Input Image Intensities and Frequencies**

We start by analyzing a 4x4 image grid with the following intensities and their corresponding frequencies:

| Intensity | Frequency |
|-----------|-----------|
| 0         | 4         |
| 75        | 6         |
| 175       | 4         |
| 255       | 2         |

### 2. **CDF Calculation**

The **Cumulative Distribution Function (CDF)** is calculated by accumulating the frequency values and dividing them by the total number of pixels in the image. The formula for CDF is:

`CDF = Cumulative Frequency / Total Pixels`

The total number of pixels is 16 (since it is a 4x4 image). The CDF calculation for each intensity is:

| Intensity | Frequency | CDF         |
|-----------|-----------|-------------|
| 0         | 4         | 4 / 16 = 0.25|
| 75        | 6         | (4 + 6) / 16 = 10 / 16 = 0.625|
| 175       | 4         | (10 + 4) / 16 = 14 / 16 = 0.875|
| 255       | 2         | (14 + 2) / 16 = 16 / 16 = 1.0|

Thus, the **CDF** values are:

`CDF = [0.25, 0.625, 0.875, 1.0]`

---

### 3. **Normalized CDF Calculation**

The **Normalized CDF** is calculated by dividing the CDF values by the total number of pixels (16). This normalizes the CDF to the range [0, 1]. The formula for Normalized CDF is:

`Normalized CDF = CDF / Total Pixels`

For our case:

| Intensity | CDF      | Normalized CDF |
|-----------|----------|----------------|
| 0         | 0.25     | 0.25 / 16 = 0.015625  |
| 75        | 0.625    | 0.625 / 16 = 0.0390625 |
| 175       | 0.875    | 0.875 / 16 = 0.0546875 |
| 255       | 1.0      | 1.0 / 16 = 0.0625      |

Thus, the **Normalized CDF** values are:

`Normalized CDF = [0.015625, 0.0390625, 0.0546875, 0.0625]`

---

### 4. **Equalized CDF Calculation**

To obtain the **Equalized CDF**, we multiply the **Normalized CDF** by 255 to scale the values to the [0, 255] intensity range. The formula for Equalized CDF is:

`Equalized CDF = Normalized CDF × 255`

The **Equalized CDF** values are:

| Intensity | Normalized CDF | Equalized CDF |
|-----------|----------------|---------------|
| 0         | 0.015625       | 0.015625 × 255 = 63.75  → 64   |
| 75        | 0.0390625      | 0.0390625 × 255 = 159.375 → 159 |
| 175       | 0.0546875      | 0.0546875 × 255 = 223.125 → 223 |
| 255       | 0.0625         | 0.0625 × 255 = 255       → 255 |

Thus, the **Equalized CDF** values are:

`Equalized CDF = [64, 159, 223, 255]`

---

### 5. **Apply Histogram Equalization**

Finally, we apply histogram equalization by mapping each original intensity value to the corresponding **Equalized CDF** value. This mapping adjusts the intensities based on the calculated CDF values to enhance the image contrast.

| Intensity | Equalized CDF |
|-----------|---------------|
| 0         | 64            |
| 75        | 159           |
| 175       | 223           |
| 255       | 255           |

So, the new intensity values after histogram equalization are:

`[64, 159, 223, 255]`

These values can now be used to remap the original image intensities and apply the contrast-enhanced version.

---

## Conclusion

- **CDF** helps to determine the cumulative probability distribution of pixel intensities.
- **Normalized CDF** scales the CDF values to the [0, 1] range.
- **Equalized CDF** is the scaled version of the normalized CDF, used for enhancing the image contrast.

By performing these steps, we improve the image contrast and make the intensity values more evenly distributed across the range [0, 255], thus achieving a better visual result.

---

## Example Code

```python
import numpy as np
import matplotlib.pyplot as plt

# Define the original intensities and their frequencies
intensities = [0, 75, 175, 255]
frequencies = [4, 6, 4, 2]

# Calculate the CDF
total_pixels = sum(frequencies)
cdf = np.cumsum(frequencies) / total_pixels

# Normalize the CDF
normalized_cdf = cdf / total_pixels

# Calculate the Equalized CDF by scaling the Normalized CDF by 255
equalized_cdf = np.round(normalized_cdf * 255).astype(int)

# Display the results
print("CDF:", cdf)
print("Normalized CDF:", normalized_cdf)
print("Equalized CDF:", equalized_cdf)

# Visualize the histograms
plt.subplot(1, 2, 1)
plt.plot(intensities, cdf, label="CDF")
plt.title('CDF')

plt.subplot(1, 2, 2)
plt.plot(intensities, equalized_cdf, label="Equalized CDF", color='r')
plt.title('Equalized CDF')

plt.show()
```