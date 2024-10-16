# Fourier Transform of a 1D Signal

## Overview

This document provides an understanding of **1D signals** and their corresponding **1D Fourier Transform**. We will explore the meaning of dimensionality in signals and the transformation from the **time/spatial domain** to the **frequency domain** using Fourier Transform. Additionally, we'll discuss how **intensity** (amplitude) is measured in the frequency domain.

---

## 1. What is a 1D Signal?

A **1D signal** (one-dimensional signal) is a function that varies with respect to a **single variable**, such as **time** or **space**. Common examples include:

- **Time-based signals**: Audio waveforms or sensor data over time.
- **Spatial signals**: Temperature or pressure values measured along a line.

These signals are described by a function, `f(x)`, where `x` could represent time or position.

### Example
- **Sound Wave**: A signal representing the variation of sound pressure over time.
- **Temperature Distribution**: A signal showing the temperature along a single path or line in space.

---

## 2. What is a 1D Fourier Transform?

The **1D Fourier Transform** takes a 1D signal and transforms it from the **time or spatial domain** into the **frequency domain**. It decomposes the original signal into a sum of sinusoidal waves (sine and cosine) of different frequencies.

### Key Points:
- The Fourier Transform helps identify the **frequency components** present in a signal.
- It provides both the **amplitude** and **phase** of each sinusoid that makes up the original signal.
- The **amplitude** represents the **intensity** of each frequency component, and the **phase** provides information about the timing of the sinusoid.

---

## 3. Why is It Called 1D?

Both the signal and the Fourier transform are referred to as **1D** (one-dimensional) because they vary along only **one variable**:
- The original signal depends on one variable (e.g., time or position).
- The Fourier Transform also results in a **1D frequency spectrum**, showing how the frequencies are distributed across the signal.

In contrast, a **2D signal** (like an image) requires a **2D Fourier Transform** because it varies along two dimensions (height and width).

---

## 4. Intensity in the Frequency Domain

The **amplitude** of each sinusoidal wave in the Fourier Transform corresponds to the **intensity** of that particular frequency component. This means the higher the amplitude, the stronger or more prominent that frequency is within the original signal.

### Example:
- In an **audio signal**, higher amplitudes at certain frequencies may represent louder sounds.
- In **image processing**, higher intensity at certain frequencies can highlight specific patterns or details in the image.

The Fourier Transform not only reveals the amplitudes (intensities) of different frequencies but also captures the **phase** of each component, which determines the exact positioning or timing of the sinusoidal waves.

---

## 5. Example of 1D Fourier Transform

Consider a **simple sound wave** that varies over time:
1. **Input Signal**: A 1D function representing sound amplitude as it changes over time.
2. **Fourier Transform**: The transform outputs a frequency spectrum that shows the different frequencies that make up the sound wave.

By applying the Fourier Transform, we can extract the **frequency components** from the original sound signal. These frequencies can tell us about the tones or pitch in the sound, and the amplitude of each frequency indicates the **intensity** of that tone.

---

## 6. How is the 1D Fourier Transform Used?

The 1D Fourier Transform is widely used in various applications:
- **Signal Processing**: To filter noise, analyze sound waves, or compress audio.
- **Image Processing (in 1D)**: To process signals along rows or columns of an image.
- **Physics and Engineering**: To analyze waveforms, vibrations, and other phenomena.

---

## Conclusion

In summary, a **1D signal** is one that depends on a single variable (such as time or space), and its **1D Fourier Transform** reveals the frequency components within the signal. This transformation is essential for signal analysis, filtering, and understanding the underlying periodicities of the signal. The Fourier Transform helps measure the **intensity** of different frequency components, providing insight into both amplitude (strength) and phase (timing) of the sinusoidal waves.