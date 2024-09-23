# Interpreting Image Intensities: Radiometric Concepts & Reflectance Properties

## Table of Contents

1. [Introduction](#introduction)
2. [Radiometry: The Study of Light](#radiometry-the-study-of-light)
   - 2.1 [What is the brightness of the source?](#what-is-the-brightness-of-the-source)
   - 2.2 [What is the illumination of the surface?](#what-is-the-illumination-of-the-surface)
   - 2.3 [What is the brightness of the surface?](#what-is-the-brightness-of-the-surface)
3. [Reflectance: Surface Light Reflection](#reflectance-surface-light-reflection)
4. [Surface Radiance](#surface-radiance)
   - 4.1 [What is surface radiance?](#what-is-surface-radiance)
   - 4.2 [What is image irradiance?](#what-is-image-irradiance)
5. [Surface Radiance & Image Irradiance Relationship](#surface-radiance--image-irradiance-relationship)
6. [Bidirectional Reflectance Distribution Function (BRDF)](#bidirectional-reflectance-distribution-function-brdf)
7. [Common Reflectance Properties in the Real World](#common-reflectance-properties-in-the-real-world)
8. [Reflectance Models](#reflectance-models)
9. [Dichromatic Model](#dichromatic-model)
   - 9.1 [Impact of Illumination Color on Reflectance](#impact-of-illumination-color-on-reflectance)
10. [Conclusion](#conclusion)

---

## Introduction

To properly interpret **image intensities**, it is crucial to understand the principles of **Radiometry** and **Reflectance**. These radiometric and photometric concepts enable us to analyze how light interacts with surfaces and how this interaction affects the resulting image. This document presents key topics, including radiometry, reflectance properties, and their role in image formation and appearance.

---

## 1. Radiometry: The Study of Light

**Radiometry** is the science of measuring electromagnetic radiation, especially light. It is essential for understanding **image intensities**, as it provides a quantitative framework for analyzing light's intensity, energy, and power.

### 1.1 What is the brightness of the source?

Brightness refers to the intensity of the light emitted by a source. It measures the radiometric power distributed across a light source in all directions.

### 1.2 What is the illumination of the surface?

Illumination represents the amount of light incident on a surface. This concept measures how much radiant energy is falling onto the surface, influencing its visibility and brightness in an image.

### 1.3 What is the brightness of the surface?

Surface brightness refers to the amount of light that is reflected or emitted from the surface. This value depends on both the amount of incident illumination and the reflectance characteristics of the surface.

---

## 2. Reflectance: Surface Light Reflection

**Reflectance** describes the behavior of surfaces when they reflect light. Surfaces vary in how they reflect light, and their reflectance properties depend on material composition, surface texture, and geometry.

- Reflectance plays a vital role in determining how a surface appears in an image.
- Reflectance also affects **surface radiance** and **image irradiance**.

---

## 3. Surface Radiance

### 3.1 What is surface radiance?

**Surface radiance** quantifies the amount of light leaving a surface in a specific direction. It is a measure of how bright a surface appears from a given viewing angle.

### 3.2 What is image irradiance?

**Image irradiance** represents the intensity of light reaching the camera sensor from the scene. This is proportional to the surface radiance and defines the brightness of the image's pixels.

---

## 4. Surface Radiance & Image Irradiance Relationship

The relationship between **surface radiance** and **image irradiance** is critical for understanding how scenes are captured in images. Image irradiance is influenced by the surface radiance, surface orientation, and distance to the camera.

- **Formula**: `E_image ∝ L_scene * (cos(θ) / r²)`

Where:
- `E_image` = Image irradiance
- `L_scene` = Scene radiance (brightness of the scene)
- `θ` = Angle of the surface normal relative to the camera
- `r` = Distance from the surface to the camera

---

## 5. Bidirectional Reflectance Distribution Function (BRDF)

The **Bidirectional Reflectance Distribution Function (BRDF)** describes how light reflects off an opaque surface, mapping the relationship between incoming and outgoing light. This function is crucial in predicting how surfaces look under different lighting conditions and viewing angles.

- BRDF is widely used in computer graphics for realistic rendering.
- It helps model the complex behavior of light interactions with real-world surfaces.

---

## 6. Common Reflectance Properties in the Real World

Surfaces exhibit different reflectance properties, including:

- **Diffuse surfaces**: Scatter light in many directions (e.g., matte or rough surfaces).
- **Specular (mirror-like) surfaces**: Reflect light in a single direction (e.g., polished metal).
- **Glossy surfaces**: Combine both diffuse and specular reflection (e.g., shiny plastics).

Understanding these properties is key to interpreting images correctly and simulating realistic lighting.

---

## 7. Reflectance Models

**Reflectance models** describe how surfaces reflect light and are used to simulate different material appearances. Popular models include:

- **Lambertian model**: For diffuse surfaces, assumes light is scattered uniformly.
- **Phong model**: For shiny surfaces, introduces specular reflection.

These models help simulate how surfaces will look under various lighting setups in imaging and computer vision applications.

---

## 8. Dichromatic Model

The **Dichromatic Reflectance Model** explains how surface reflections are influenced by the material properties of the surface and the color of the light source. It models both diffuse and specular components of reflection.

### 8.1 Impact of Illumination Color on Reflectance

The color of the illuminating light affects the color of the reflected light. For example, a white surface illuminated by red light will appear red, as it reflects the color components of the incident light.

---

## Conclusion

Understanding **Radiometry** and **Reflectance** is fundamental to interpreting **image intensities**. These concepts describe how light interacts with surfaces and is captured by imaging systems, leading to accurate image analysis and realistic computer-generated imagery.

By mastering these principles, you can improve image processing tasks, computer vision, and realistic rendering applications.
