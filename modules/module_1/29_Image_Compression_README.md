# Image Compression and Color Representation

## Introduction
The last stage in a camera’s processing pipeline is usually some form of image compression (unless you are using a lossless compression scheme such as camera RAW or PNG). All color video and image compression algorithms start by converting the signal into YCbCr (or some closely related variant) to compress the luminance signal with higher fidelity than the chrominance signal.

## Key Concepts

### Interchangeability of Y and I
- **Intensity (I)** typically refers to the physical amount of light or the power per unit area that a pixel receives. It may not always account for how the human eye perceives brightness.
- While **Y (luminance)** and **I (intensity)** can both represent brightness, **Y** is more perceptually relevant, reflecting how brightness is perceived by the human eye. In contrast, **I** can refer to the raw intensity of light without accounting for human perception.


### Luminance (Y) and Chrominance (Cb and Cr)
- **Luminance (Y)**: 
  - Luminance is a measure of the brightness of a pixel, specifically as perceived by the human eye. It quantifies the amount of light emitted, reflected, or transmitted by a surface in a way that corresponds to human vision.
  - In the **YCbCr color space**, Y represents the luminance component, which is derived from the RGB values of a pixel.

- **Chrominance (Cb and Cr)**: 
  - Chrominance represents the color information in an image. 
  - **Cb** (blue-difference chroma) and **Cr** (red-difference chroma) are derived from the RGB values and indicate how much blue or red is present in the image relative to the luminance.

## Image Compression Process
1. **Conversion to YCbCr**: 
   - Color video and image compression algorithms convert RGB signals into YCbCr to enhance luminance fidelity.
  
2. **Subsampling**: 
   - It is common to subsample Cb and Cr by a factor of two horizontally, with still images (JPEG) subsampling both horizontally and vertically.

3. **Block Transform Stage**: 
   - Luminance and chrominance images are passed to a block transform stage, commonly using the discrete cosine transform (DCT).

4. **Quantization**: 
   - After transform coding, coefficient values are quantized into small integer values that can be coded using variable bit-length schemes such as Huffman coding.

5. **Motion Compensation**: 
   - In video compression, block-based motion compensation encodes the difference between each block and a predicted set of pixel values.

6. **Compression Quality**: 
   - The quality of a compression algorithm is usually reported using its peak signal-to-noise ratio (PSNR), derived from the average mean square error (MSE).

## References
- Szeliski, Richard. *Computer Vision: Algorithms and Applications*. Springer International Publishing.
- Wang, Z., & Bovik, A. C. (2009). "Mean Squared Error: Love It or Leave It?" *IEEE Signal Processing Magazine*, 26(1), 98-117.
