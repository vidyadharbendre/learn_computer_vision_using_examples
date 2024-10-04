# Transition from Poisson to Gaussian Distribution in Photon Arrival

In the previous section, we discussed how the **Poisson distribution** models the random arrival of photons at image sensor pixels, especially in low-light conditions where the photon count is low. However, as the number of incoming photons increases, the Poisson distribution begins to approximate a **Gaussian (Normal) distribution**.

## Transition with Increasing Mean

The Poisson distribution is defined by a single parameter: the **mean** (denoted by λ). This parameter represents the average number of photons hitting a pixel per unit time. Importantly, this mean value is directly linked to the **brightness** of the scene at a specific point. 

- **Low mean values** (low photon counts) correspond to **darker areas** in the scene.
- **High mean values** (high photon counts) correspond to **brighter areas** in the scene.

As the mean photon count increases—especially when the mean exceeds 10—the Poisson distribution begins to resemble a **Gaussian distribution**.

### Why the Transition to Gaussian?

- When the photon count (mean) is **low**, the variance is also low, and the distribution is skewed, making the **Poisson distribution** a better model.
- As the mean increases (indicating more photons and thus higher brightness), the variance grows, but the distribution becomes more symmetric, eventually resembling a **Gaussian distribution**.
- For **mean photon counts above 10**, the Poisson distribution closely approximates the **bell curve** shape of a Gaussian distribution.

### Example: Mean Increasing Above 10

Imagine that instead of a low-light scenario where only a few photons hit the pixel, now we are dealing with a scenario where there is ample lighting:

- Instead of the random arrival of 3-4 photons, we now have **dozens** or even **hundreds** of photons arriving per unit time, correlating to the **brighter portions** of the image.
- As the photon count per pixel increases, the randomness is still present, but the overall distribution becomes smoother and more predictable, following a **Gaussian pattern**.

### Mean Value and Scene Brightness

The **mean value** of the photon count at each pixel is directly tied to the **brightness of the scene point** being captured by that pixel. 

- In **darker regions**, fewer photons reach the sensor, resulting in a **lower mean**.
- In **brighter regions**, more photons reach the sensor, leading to a **higher mean**.

Thus, the brightness of a scene point can be measured by the average number of photons that hit the corresponding pixel in a given time period.

### Why is This Important?

This transition from Poisson to Gaussian helps simplify mathematical models as the photon count increases, particularly in **brighter areas** of the image. Since **Gaussian distributions** are easier to handle in image processing algorithms, many techniques in **high-light environments** assume a Gaussian noise model rather than a Poisson one.

## Key Takeaway

- **Low photon counts** (low mean, darker areas) ➡️ **Poisson distribution** is the best model.
- **High photon counts** (mean > 10, brighter areas) ➡️ **Poisson distribution** starts approximating a **Gaussian distribution**.
- This approximation allows for better **image denoising** and **processing algorithms** in brighter environments, making image sensors more efficient and adaptable to different lighting conditions.

---

Understanding this transition is essential for designing robust image sensors and processing algorithms that can handle a wide range of lighting conditions—from low light (where Poisson noise dominates) to well-lit environments (where Gaussian noise can be assumed). The mean photon count not only helps us model noise but is also an important metric for **measuring the brightness of the scene points** being captured.
