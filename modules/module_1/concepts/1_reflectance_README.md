# Reflectance: Understanding Light Interaction with Objects

## Introduction
**Reflectance** is the process by which light interacts with the surface of an object and is either absorbed, scattered, or reflected. This concept is key in understanding how light behaves when it strikes an object and how cameras capture that light to form an image.

In this document, we'll explore how light interacts with a single point on an object (e.g., a strawberry in a bowl), how the reflected light reaches a camera, and how the camera translates this light into an **image intensity value** at a specific point. The intensity value will be represented as a **6-digit hexadecimal code**, corresponding to the RGB color channels.

## 1. Illumination
When light from a source (such as the sun or a light bulb) strikes the surface of an object, it illuminates the object. Consider a single point on the strawberry:

- Light is composed of various wavelengths, which correspond to different colors.
- This light hits the surface of the strawberry, initiating the interaction that leads to reflection, absorption, or scattering.

## 2. Interaction at the Surface (Reflectance)
The nature of light interaction at the surface of the strawberry depends on the material properties of the object, including:

- **Color**: A red strawberry absorbs most wavelengths except red, which it reflects.
- **Surface texture**: Whether the surface is smooth or rough will affect how light is scattered or reflected.

### Types of Reflection:
- **Diffuse Reflection**: Light is scattered in multiple directions due to a rough surface.
- **Specular Reflection**: Light is reflected in a single direction from smooth surfaces.

At this stage, some light is absorbed by the surface, while some is reflected or scattered in various directions.

## 3. Scattering in the Direction of the Camera
Some of the reflected or scattered light reaches the camera lens. The amount of light scattered in the direction of the camera depends on:

- The **angle of incidence** (the angle at which the light strikes the surface).
- The **surface material** (whether the strawberry's skin is glossy or matte).
  
The light that reaches the camera passes through the lens and is focused onto the **image plane**.

## 4. Image Intensity at a Single Point
Once the light from the specific point on the strawberry reaches the camera sensor, the camera records an **intensity value** for that point. This value corresponds to the brightness or darkness of the pixel representing that point in the final image. 

### Intensity Representation in RGB Hexadecimal
The intensity value is commonly represented as a **6-digit hexadecimal code**, where:
- The first two digits represent the intensity of the **Red (R)** channel.
- The next two digits represent the intensity of the **Green (G)** channel.
- The last two digits represent the intensity of the **Blue (B)** channel.

For example, an intensity value of `#FF5733` represents:
- **Red (R)**: `FF` in hex (255 in decimal).
- **Green (G)**: `57` in hex (87 in decimal).
- **Blue (B)**: `33` in hex (51 in decimal).

This RGB value determines the color and brightness of the pixel at that specific point on the strawberry in the image.

### Factors Affecting Image Intensity:
- **Material Properties**: The color and texture of the object’s surface.
- **Lighting Conditions**: The strength, direction, and quality of the light source.
- **Camera Settings**: Exposure time, aperture, and sensitivity (ISO).
- **Angle of Incidence**: How the light source is positioned relative to the object and camera.

The intensity value recorded by the camera is thus a combination of the **light reflection** and **camera settings**, determining the color and brightness of the point in the image.

## 5. Conclusion
Reflectance is a fundamental concept in understanding how light interacts with objects and how cameras capture this interaction to form images. By examining a single point on an object like a strawberry, we can observe how light is reflected, scattered, and captured, resulting in the intensity values that form an image.

The **RGB hexadecimal representation** of the intensity value further helps quantify the light interaction, giving a precise color value that can be used in digital image processing and photography.
