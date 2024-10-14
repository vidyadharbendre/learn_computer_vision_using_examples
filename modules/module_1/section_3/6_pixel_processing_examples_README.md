# Pixel Processing Examples

## 1. Pixel Processing Overview
Pixel processing (also called **point processing**) involves applying a transformation to each pixel independently of its neighbors. These transformations can adjust brightness, contrast, or invert the pixel values.

For each pixel at `(x, y)` in the image, the original intensity value `f(x, y)` can be modified according to various pixel-level operations.

## 2. Common Pixel Transformations

### 2.1 Darkening an Image
To **darken** an image, we subtract a constant value from the intensity of each pixel. This effectively shifts the pixel values towards the darker end of the intensity spectrum.

- **Formula**: `g(x, y) = f(x, y) - 128`
- **Effect**: The brightness of every pixel is reduced by 128, making the image appear darker.

### 2.2 Lightening an Image
To **lighten** an image, we add a constant value to the intensity of each pixel, shifting it towards the lighter end of the intensity spectrum.

- **Formula**: `g(x, y) = f(x, y) + 128`
- **Effect**: The brightness of every pixel is increased by 128, making the image appear brighter.

### 2.3 Inverting an Image
To **invert** an image, we replace each pixel’s intensity with its complementary value relative to the maximum intensity (255 for an 8-bit grayscale image).

- **Formula**: `g(x, y) = 255 - f(x, y)`
- **Effect**: The intensity values are flipped. Dark areas become bright, and bright areas become dark.

## 3. Examples

Given an image with a pixel value `f(x, y)`:
- **Original pixel**: `f(x, y) = 100`
  
  The pixel transformations would result in:
  - **Darkened pixel**: `g(x, y) = 100 - 128 = -28` (values less than 0 are clamped to 0)
  - **Lightened pixel**: `g(x, y) = 100 + 128 = 228`
  - **Inverted pixel**: `g(x, y) = 255 - 100 = 155`

---

These transformations are basic but powerful techniques in image processing for adjusting the overall tone and contrast of an image. They are commonly used in applications where simple brightness control or special effects are desired.
