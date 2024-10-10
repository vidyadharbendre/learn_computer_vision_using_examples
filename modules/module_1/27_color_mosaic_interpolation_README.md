# Demosaicing and Bayer Pattern - A Simple Explanation

### Overview

In digital imaging, most sensors capture light using a **color filter array (CFA)** to convert the incoming light into digital data. The **Bayer pattern** is the most commonly used CFA. It captures red, green, and blue light by arranging them in a grid of pixels. However, since each pixel can only capture **one color** (either red, green, or blue), the process of **demosaicing** is needed to reconstruct a full-color image from this data.

### Bayer Filter Pattern

The **Bayer pattern** is a mosaic-like filter placed on top of the image sensor. Each pixel is covered by a red, green, or blue filter, allowing it to capture only one of those colors. The pattern is arranged so that 50% of the pixels are sensitive to **green** (since the human eye is most sensitive to green), 25% to **red**, and 25% to **blue**.

Example of a Bayer pattern:

G R G R G R B G B G B G G R G R G R B G B G B G

- **G** = Green
- **R** = Red
- **B** = Blue

### How It Works

Each pixel only captures **one color** (either Red, Green, or Blue). For example:
- A pixel under a **green filter** only captures the intensity of green light.
- A pixel under a **red filter** only captures the intensity of red light.
- A pixel under a **blue filter** only captures the intensity of blue light.

However, this means that each pixel is missing the other two colors. To create a complete color image, the missing colors must be **interpolated** from neighboring pixels.

### Step-by-Step Process of Demosaicing

1. **Capture Light:** The sensor captures light through the Bayer filter, and each pixel only stores the intensity of **one color** (Red, Green, or Blue).
   
2. **Interpolation (Finding Missing Colors):**
   - For a **green pixel**, the algorithm estimates the **red** and **blue** values based on nearby red and blue pixels.
   - For a **red pixel**, the algorithm estimates the **green** and **blue** values from neighboring green and blue pixels.
   - Similarly, for a **blue pixel**, the algorithm estimates the **red** and **green** values.

3. **Reconstruct Full Color Image:** The final step is reconstructing the full-color image by assigning red, green, and blue values to every pixel. This process is called **demosaicing**.

### Example

1. **Input Data:**
   - Each pixel captures one color.
   
2. **Missing Data:**
   - For each red, green, or blue pixel, the missing color values are interpolated using the surrounding pixels.

3. **Final Image:**
   - After interpolation, each pixel has full **RGB values**, allowing us to display the image as a complete color photo.

### Conclusion

The process of **demosaicing** allows digital cameras to turn the data captured by a **Bayer-filtered sensor** into a complete, full-color image. Without demosaicing, each pixel would only have partial color information, but with this method, every pixel is able to contribute to a rich, full-color image.

