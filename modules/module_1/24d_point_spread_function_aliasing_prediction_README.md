# Point Spread Function (PSF) and Aliasing Prediction

## Understanding PSF

The best way to predict the amount of aliasing produced by an imaging system (or image processing algorithm) is to estimate the **Point Spread Function (PSF)**. The PSF represents the response of a pixel sensor to an ideal point light source and combines the blur induced by the optical system (lens) and the finite integration area of a chip sensor.

### Convolution and Fourier Transform

If we know the blur function of the lens and the fill factor of the imaging chip, we can convolve these functions to obtain the PSF. Taking the Fourier transform of the PSF yields the **Modulation Transfer Function (MTF)**, which helps estimate the amount of aliasing.

---

## References

- Szeliski, Richard. *Computer Vision: Algorithms and Applications* (Texts in Computer Science). Springer International Publishing.
