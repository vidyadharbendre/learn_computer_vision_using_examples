# Modeling Photon Arrival Using Poisson Distribution

When light from a source hits the image sensor, photons arrive at each pixel (which can be thought of as tiny buckets) over a period of time. However, the number of photons arriving at any given pixel isn't consistent or uniform. Instead, it's a random process where:

- Sometimes 3-4 photons might hit the pixel.
- Other times, 6-7 photons may arrive.
- In some cases, no photons will arrive at all.

This variability in photon arrival is a result of the **quantum nature of light**, which leads to randomness in how photons reach the sensor.

## Modeling Photon Arrival with Poisson Distribution

The random nature of photon arrival can be effectively modeled using a **Poisson distribution**, which is commonly used to describe events that happen independently over a fixed period of time or space. In the case of image sensors:

- The **Poisson distribution** helps in modeling the number of photons arriving at each pixel per unit time.
- It is particularly useful in **low-light conditions**, where the variability in photon count is more pronounced.

### Why Poisson Distribution?

- The **Poisson distribution** is suitable for cases where events (photon arrivals) occur randomly and independently.
- It allows us to predict the probability of a given number of photons hitting a pixel in a specific time frame, which is crucial for understanding and managing **shot noise** in image sensors.

### Example

Imagine a pixel in an image sensor as a bucket, and photons are like raindrops falling into the bucket over time. Sometimes, only a few raindrops (photons) fall, other times more, and occasionally none at all. By using the Poisson distribution, we can model the likelihood of these different photon counts and account for the resulting noise in the final image.

This model helps in designing noise reduction algorithms, improving image quality, especially in **low-light environments**, and ensuring that the captured images are more accurate and less affected by the inherent randomness of photon arrival.

---

By understanding photon arrival through the lens of Poisson distribution, we can better anticipate and handle the **shot noise** caused by these variations, leading to more sophisticated image sensor technologies and improved image processing techniques.
