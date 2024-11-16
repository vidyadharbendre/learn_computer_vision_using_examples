# Histogram Equalization: A Practical Example

Let's walk through the process of Histogram Equalization with a practical example to better understand how values are applied during the equalization process. I'll use a simple, synthetic grayscale image to make it easier to explain how the pixel intensities are redistributed.

## Example 1: Understanding Histogram Equalization with a Simple Image

### 1. Original Image and Its Histogram
Imagine we have a grayscale image with the following pixel intensities:

| Pixel Intensity (Value) | Number of Pixels |
|-------------------------|------------------|
| 10                      | 2                |
| 20                      | 3                |
| 50                      | 1                |
| 100                     | 1                |
| 150                     | 3                |
| 200                     | 2                |
| 250                     | 3                |

This means:
- There are 2 pixels with intensity 10,
- There are 3 pixels with intensity 20,
- There is 1 pixel with intensity 50, and so on.

### 2. Histogram of the Original Image
The histogram of the original image would look something like this:

- The x-axis represents pixel intensities (0-255),
- The y-axis represents the frequency of each intensity.

The histogram might have gaps and be "concentrated" around certain values, such as 10, 20, 150, and 250. This distribution suggests that the image might be too dark in some areas (low intensity) and too bright in others (high intensity).

### 3. Cumulative Distribution Function (CDF)
The next step in histogram equalization is to compute the Cumulative Distribution Function (CDF) for the pixel intensities. The CDF shows how the pixel values accumulate across the image.

The CDF is computed as the cumulative sum of the histogram values, starting from the lowest intensity:

- For intensity 10: `CDF = 2` (because there are 2 pixels with intensity 10),
- For intensity 20: `CDF = 2 + 3 = 5` (because there are 3 pixels with intensity 20),
- For intensity 50: `CDF = 5 + 1 = 6` (because there is 1 pixel with intensity 50),
- For intensity 100: `CDF = 6 + 1 = 7`,
- For intensity 150: `CDF = 7 + 3 = 10`,
- For intensity 200: `CDF = 10 + 2 = 12`,
- For intensity 250: `CDF = 12 + 3 = 15`.

### 4. Normalize the CDF
Now, we normalize the CDF. To do this, we divide each value in the CDF by the total number of pixels (15 pixels in this case) and then multiply by 255 (the maximum pixel intensity):

'Normalized CDF = (CDF / Total Pixels) × 255'

So for each intensity, we apply the following:

- For intensity 10: `2 / 15 × 255 ≈ 34`,
- For intensity 20: `5 / 15 × 255 = 85`,
- For intensity 50: `6 / 15 × 255 ≈ 102`,
- For intensity 100: `7 / 15 × 255 ≈ 119`,
- For intensity 150: `10 / 15 × 255 = 170`,
- For intensity 200: `12 / 15 × 255 = 204`,
- For intensity 250: `15 / 15 × 255 = 255`.

This results in the following normalized CDF:

| Pixel Intensity (Original) | Normalized CDF (Equalized) |
|----------------------------|----------------------------|
| 10                         | 34                         |
| 20                         | 85                         |
| 50                         | 102                        |
| 100                        | 119                        |
| 150                        | 170                        |
| 200                        | 204                        |
| 250                        | 255                        |

### 5. Mapping Original Intensities to New Intensities
Now we use the normalized CDF to map the original pixel intensities to new intensities. The new pixel intensity values will be distributed more uniformly across the full range (0 to 255).

- Pixels with an intensity of 10 will now have an intensity of 34,
- Pixels with an intensity of 20 will now have an intensity of 85,
- Pixels with an intensity of 50 will now have an intensity of 102, and so on.

This process redistributes the pixel intensities across the entire range, improving the contrast of the image.

### 6. Result: Equalized Image
The equalized image now has pixel intensities that are more evenly spread across the entire range of 0-255. It will appear with improved contrast, where both dark and light areas of the image are enhanced.

- In the original image, the pixel intensities were concentrated in the lower range (10-250), which might have caused some areas of the image to appear too dark or too bright.
- After equalization, the intensities are more evenly distributed, making the details in both dark and bright areas more visible.
