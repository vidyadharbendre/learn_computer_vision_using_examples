# Noise in Image Sensors

Noise is an unavoidable part of image sensing, and it can arise from various sources during the capture and processing of images. Understanding these noise types is essential for optimizing image quality, especially in fields like computer vision and digital photography.

## Types of Noise

### 1. Scene Dependent Noise
This type of noise is dependent on the lighting conditions and the characteristics of the scene being captured.

#### Photon Shot Noise
- **Quantum Nature of Light**: Due to the quantized nature of light, photons do not arrive at the sensor in a uniform manner, leading to randomness in photon counts.
- **Random Arrival of Photons**: The arrival of photons follows a random distribution, typically modeled using a Poisson distribution, particularly in low-light conditions.

### 2. Scene Independent Noise
Scene-independent noise arises from the sensor and processing components, regardless of the scene or lighting.

#### Readout Noise
- **Electronic Noise**: Occurs in the sensor's readout circuit before the signal is converted from analog to digital. This noise is inherent in the electronics of the sensor.
- **Quantization Noise**: Introduced during the analog-to-digital conversion (ADC). When continuous analog values are converted into discrete digital numbers, some loss of information occurs, resulting in quantization noise.

#### Other Sources of Noise
- **Dark Current Noise**: Caused by thermally generated electrons in the sensor, even when no light is present. This noise increases with higher temperatures.
- **Fixed Pattern Noise (FPN)**: This type of noise is caused by irregularities or defects in individual sensor pixels. It remains constant for a given sensor but varies from one sensor to another.

## Noise Throughout the Sensing Process

Throughout the entire image sensing pipeline, noise is introduced from various sources, including:
- **Fixed Pattern Noise**
- **Dark Current Noise**
- **Photon Shot Noise**
- **Amplifier Noise**
- **Quantization Noise**

The final amount of noise in the sampled image depends on factors like:
- The **incoming light** (scene radiance and aperture)
- **Exposure time**
- **Sensor gain**

### Poisson vs. Gaussian Noise Models
For **low light conditions**, where the noise is due to a low number of photons, a **Poisson model** is more appropriate for capturing noise characteristics. However, in more generalized scenarios, a **Gaussian noise model** may be used to describe noise distributions.

### Estimating Noise Levels
To optimize noise reduction or image processing algorithms (e.g., denoising, edge detection), it's crucial to estimate noise levels. One approach is to use:
- **Noise Level Function (NLF)**: This function predicts the overall noise variance at a given pixel as a function of its brightness. This can be estimated for each color channel individually.
  
Alternatively, one can **pre-calibrate the NLF** by taking multiple shots of a color calibration chart (e.g., the Macbeth Color Chart) to measure noise variance under different exposure times and gain settings.

### Practical Applications
In computer vision and image processing, **image denoising**, **edge detection**, and **stereo matching** can all benefit from accurate noise estimation. Even without pre-calibration, noise variance can be estimated from regions of near-constant brightness in the image.

---

### Summary

Understanding the various types of noise—whether scene dependent or independent—along with their causes and how they manifest, is essential for improving the performance of digital cameras and image sensors. Proper noise estimation helps in optimizing image processing algorithms and obtaining cleaner, more accurate images.
