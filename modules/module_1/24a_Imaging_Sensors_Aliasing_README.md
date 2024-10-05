# Introduction to Imaging Sensors and Aliasing

## What Happens When Light Impinges on Image Sensors?

When a field of light impinges on an image sensor, it interacts with the active sense areas of the imaging chip. The photons arriving at each active cell are integrated and subsequently digitized. However, if the fill factor on the chip is small and the signal is not otherwise band-limited, visually unpleasing aliasing can occur.

## Understanding Aliasing

Aliasing occurs when different signals become indistinguishable from each other when sampled. For instance, consider two sine waves at frequencies 'f = 3/4' and 'f = 5/4'. When these signals are sampled at a frequency of 'f = 2', they produce identical samples, leading to aliasing. This phenomenon hinders the reconstruction of the original signal, making it impossible to determine which frequency was present.

---

## References

- Szeliski, Richard. *Computer Vision: Algorithms and Applications* (Texts in Computer Science). Springer International Publishing.
