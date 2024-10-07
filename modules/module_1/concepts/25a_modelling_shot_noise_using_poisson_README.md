# Shot Noise Modeling Using Poisson Distribution

## Introduction

Photon noise, also known as **shot noise**, is a fundamental type of noise in image sensors and other optical systems. It arises from the discrete nature of light and the random arrival of photons on the sensor. Since the number of photons hitting the sensor is random, the variations in photon count can cause visible noise in the resulting image, especially in low-light conditions. This noise is described using the **Poisson distribution**, which models random, independent events such as photon arrivals over a fixed time period or area.

## Poisson Distribution in Photon Arrival

The Poisson distribution is a probability distribution used to model the number of events occurring in a fixed interval of time or space, given an average rate of events. In the case of photons hitting an image sensor, the events are the photon arrivals, and the average rate is related to the brightness or intensity of the light.

### Poisson Distribution Formula

The probability of observing **K** photon arrivals in a given time interval, given an average arrival rate **λ** (the brightness), is given by the Poisson distribution formula:

`P(K; λ) = (λ^K * e^(-λ)) / K!`

Where:
- `P(K; λ)` is the probability of observing `K` photon arrivals.
- `λ` is the average number of photon arrivals (mean), related to the brightness of the light source.
- `K` is the actual number of photon arrivals (a discrete random variable).
- `e` is Euler’s number, approximately `2.71828`.

### Understanding the Terms:
- **λ (Average Photon Rate):** In photon counting, **λ** represents the brightness or the expected number of photons hitting a pixel per unit of time or area. A higher **λ** means higher brightness and thus more photon arrivals.
- **K (Photon Count):** The actual number of photons that arrive in a given time or area. Due to the random nature of photon arrivals, **K** varies even if **λ** is constant.

### Example:
If the average number of photons arriving at a pixel is **λ = 10** per second, we can compute the probability of observing **K = 7** photons in that second as:

`P(7; 10) = (10^7 * e^(-10)) / 7! ≈ 0.090`

This means there is a 9% chance that exactly 7 photons will arrive in that second.

## Relation to Shot Noise

Shot noise arises because of the inherent randomness in photon arrivals. Since photons arrive independently of one another, the fluctuations in their count follow a Poisson distribution. In image sensors, this random variation in photon count leads to pixel-to-pixel noise, especially under low-light conditions where the photon count is small.

### Key Points:
- **Photon Noise or Shot Noise:** Variations in the number of photons detected by a pixel due to the random arrival of photons.
- **Low-Light Conditions:** The effect of shot noise becomes more pronounced in low-light conditions because the number of arriving photons is smaller, increasing the variability.
- **Poisson Nature:** The shot noise follows the Poisson distribution, where the mean arrival rate **λ** represents the brightness of the light source, and the variability in photon count introduces noise.

## Practical Application

In low-light imaging, the number of photons arriving at each pixel fluctuates, leading to shot noise. To accurately model this noise, the Poisson distribution is used. This statistical model is essential for understanding and improving the quality of images captured in such conditions, where the noise can significantly affect the signal.

When working with modern image sensors, understanding the relationship between photon noise and the Poisson distribution can help in designing algorithms that reduce noise, particularly in low-light environments such as astronomy or medical imaging.

## Conclusion

The Poisson distribution is a powerful tool for modeling shot noise in image sensors. It describes how photon arrivals, which are random and independent events, contribute to the noise seen in images, especially under low-light conditions. Understanding and applying this model is crucial for improving image quality in various applications, such as digital cameras and scientific imaging systems.

---

This `README.md` document provides a clear introduction to shot noise modeling using the Poisson distribution, highlighting its application in image sensors. It can serve as a useful guide for anyone looking to understand how photon noise affects imaging systems and how statistical models like the Poisson distribution can be used to describe it.
