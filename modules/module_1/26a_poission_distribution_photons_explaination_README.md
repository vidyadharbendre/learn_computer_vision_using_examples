# Photon Arrivals and Poisson Distribution in Image Sensors

## Introduction
In image sensors, photons arriving or falling on a surface (such as a pixel) is a random process. The **Poisson distribution** is a powerful statistical tool that helps describe the probability of a certain number of photon arrivals over a given period of time or in a specific area. This is particularly useful in modeling random, independent events like photon arrivals, especially in low-light imaging situations.

---

## Table of Contents
- [Poisson Distribution Basics](#poisson-distribution-basics)
- [What Each Term Represents](#what-each-term-represents)
- [Poisson Distribution for Photon Counting](#poisson-distribution-for-photon-counting)
- [Example of Application](#example-of-application)
- [When to Use the Poisson Distribution](#when-to-use-the-poisson-distribution)
- [Key Takeaways](#key-takeaways)

---

## Poisson Distribution Basics

The Poisson distribution gives the probability of observing `K` events (such as photon arrivals) in a fixed interval of time or space, given an average rate `λ` of events. This formula models how photon arrivals are distributed in time or area. The formula for the Poisson distribution is:

`P(K; λ) = (λ^K * e^(-λ)) / K!`

Where:
- **`P(K; λ)`**: Probability of observing `K` photon arrivals.
- **`λ`**: The average number of photons arriving (mean) in the given time or area, related to brightness.
- **`K`**: The actual number of photon arrivals (the random variable or "event count").
- **`e`**: Euler's number (approximately 2.71828).

---

## What Each Term Represents

### `λ` (mean or average rate of arrivals):
In the context of photons, `λ` represents the **brightness** of the light source. It is the average number of photons arriving per pixel, per unit time, or per unit area. The higher the brightness, the higher the expected number of photons (higher `λ`).

### `K` (actual number of arrivals):
`K` represents the **actual number of photons** arriving at a pixel or a specific location in a given time period. It is a **discrete random variable** in this distribution, representing the number of photon arrivals.

---

## Poisson Distribution for Photon Counting

In imaging sensors, the number of photons arriving at a pixel is random and follows a Poisson distribution. This is because the arrival of each photon is an independent event, and the number of photons arriving over a short time can vary even if the brightness (average rate `λ`) is constant.

---

## Example of Application

Suppose a sensor pixel receives photons from a light source, and on average, `λ = 10` photons hit the pixel per second. The Poisson distribution can tell us the probability of receiving exactly `K = 7`, `K = 10`, or any other number of photons during a given second.

For `λ = 10` and `K = 7`, the probability is calculated as:

`P(7; 10) = (10^7 * e^(-10)) / 7! ≈ 0.090`

This means there is a **9% chance** that exactly 7 photons will arrive in a given second when the average number is 10.

---

## When to Use the Poisson Distribution

1. **Low-light or Photonic Events**: The Poisson distribution is particularly important in **low-light conditions** (e.g., astronomy, medical imaging, or photon-counting cameras). In such cases, the photon count is often low and random, and Poisson statistics give an accurate model of this behavior.
   
2. **Photon Noise**: In image sensors, **photon noise** (or "shot noise") arises due to the random variation in the number of photons detected per pixel. This noise follows a Poisson distribution because photon arrivals are independent random events.

---

## Key Takeaways

- **`λ`** represents the brightness or the average number of photon arrivals.
- **`K`** is the actual number of photon arrivals that we observe.
- The Poisson distribution helps model the random and independent nature of photon arrivals, especially in **low-light imaging** where the number of photons per pixel fluctuates from frame to frame.

In conclusion, the Poisson distribution is applied when we want to model or understand the probability of receiving a specific number of photons at a sensor (e.g., in a pixel), based on the average brightness of the scene (i.e., `λ`). It helps in understanding how **photon noise** affects image quality.
