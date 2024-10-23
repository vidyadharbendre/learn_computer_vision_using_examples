# ## Sensor Noise in Image Sensors

### Introduction

**Sensor noise** refers to the unwanted variations in the electrical signal produced by an image sensor. It degrades image quality by adding random speckles or graininess, particularly in low-light conditions. Noise becomes more prominent when the sensor struggles to capture sufficient light or when higher analog gain (ISO) settings are applied to brighten the image. Throughout the sensing process, noise can originate from multiple sources, such as **fixed pattern noise**, **dark current noise**, **shot noise**, **amplifier noise**, and **quantization noise** (Healey and Kondepudy 1994; Tsin, Ramesh, and Kanade 2001).

---

### How Sensor Noise Works

Sensor noise arises from various sources, with the final amount of noise depending on factors like the **incoming light** (controlled by the scene radiance and aperture), **exposure time**, and **sensor gain**. In low-light conditions, where the noise is due to low photon counts, a **Poisson noise model** may be more appropriate than the traditional Gaussian model (Alter, Matsushita, and Tang 2006; Matsushita and Lin 2007a).

The most common types of sensor noise include:

- **Read Noise**: Occurs during the process of reading the charge from the sensor and affects all images, even in ideal lighting conditions.
  
- **Shot Noise**: Results from the inherent randomness of photon capture and is more prominent in low-light situations, where fewer photons are detected.
  
- **Dark Current Noise**: Caused by thermal energy in the sensor, generating unwanted electrons even when no light is present.

The total noise present in a sampled image depends on all these factors. Advanced approaches to estimating sensor noise, like the **Noise Level Function (NLF)**, predict the overall noise variance at a given pixel based on its brightness. This method leverages empirical data, such as camera response functions (CRFs) (Grossberg and Nayar 2004), to provide more accurate noise estimates (Liu, Szeliski et al. 2008).

---

### Pre-Calibration and Estimation

For applications that require precise noise control, pre-calibrating the sensor by taking repeated shots of a scene with varying colors and luminances, such as the **Macbeth Color Chart**, can help estimate the noise variance under different exposure times and gain settings. When estimating variance, it's crucial to ignore or downweight pixels with large gradients, as minor shifts between exposures can affect sensed values.

In practical applications, such as **image denoising**, **edge detection**, and **stereo matching**, an estimate of the noise level is valuable. If pre-calibration isn't possible, a simpler method is to identify regions of constant value within an image and estimate the noise variance from these regions (Liu, Szeliski et al. 2008).

---

### Examples:

- **High Sensor Noise**: Often seen in low-light environments where the sensor operates at higher ISO settings or extended exposure times. This usually results in grainy or noisy images, especially in shadowed areas.
  
- **Low Sensor Noise**: Achieved in well-lit environments with lower ISO settings, where the sensor captures enough light to produce cleaner and sharper images with minimal graininess.

---

### Conclusion

Sensor noise is an unavoidable aspect of image capture but understanding and managing it is crucial for optimizing image quality. By controlling exposure settings, sensor design, and employing advanced noise estimation methods, it’s possible to minimize noise and improve image clarity, particularly in challenging low-light conditions.

---

### Further Reading

- [Analog Gain](#)
- [ISO](#)
- [Shutter Speed](#)
