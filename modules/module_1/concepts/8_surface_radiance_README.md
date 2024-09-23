# Surface Radiance

## Introduction

**Surface Radiance** is a radiometric quantity that measures the amount of radiant power emitted, reflected, transmitted, or received by a surface in a specific direction, per unit area and per unit solid angle. It is one of the most fundamental quantities in radiometry, particularly when analyzing the distribution of light in scenes and understanding how objects appear when illuminated.

## 1. Definition

**Radiance (L)** is defined as the amount of radiant flux (`Φ`) passing through or emitted from a surface, per unit area, per unit solid angle, in a specific direction.

- **Unit**: Watts per square meter per steradian (`W/m²·sr`)
- **Formula**: `L = d²Φ / (dA · cos(θ) · dω)`
  
  where:
  - `L` is the radiance,
  - `d²Φ` is the differential radiant flux,
  - `dA` is the differential area,
  - `θ` is the angle between the surface normal and the direction of the emitted light,
  - `dω` is the differential solid angle.

## 2. Components of Radiance

### 2.1 Area

Radiance is dependent on the **projected area** of the surface, meaning the area that is seen from the light source's point of view. This is why `cos(θ)` is included in the formula, to account for how the effective area decreases as the angle between the light direction and the surface increases.

### 2.2 Solid Angle

Radiance also takes into account the **solid angle (dω)**, which describes the amount of the 3D space subtended by the light. The solid angle is typically expressed in steradians (`sr`), and it defines the directional spread of the radiated light.

## 3. Radiance as a Directional Quantity

Radiance is a **directional quantity**: it describes how much light is traveling in a particular direction. This makes radiance different from irradiance, which simply measures the total power per unit area without considering the directionality of the light.

- **Directional Dependency**: Radiance depends on the orientation of the surface and the direction from which the light is observed. As the angle of the surface relative to the incoming light increases, the observed radiance changes.

## 4. Radiance Formula in Different Forms

### 4.1 Standard Radiance Formula

- **Formula**: `L = d²Φ / (dA · cos(θ) · dω)`
  
  where:
  - `L` is the radiance,
  - `d²Φ` is the differential radiant flux,
  - `dA` is the surface area,
  - `cos(θ)` accounts for the angle between the surface and the light,
  - `dω` is the solid angle.

### 4.2 Alternative Radiance Expression

Using the concept of **radiant intensity (I)** and **distance (r)** from the light source, we can express radiance as:

- **Formula**: `L = (I / r²) cos(θ)`
  
  where:
  - `L` is the radiance,
  - `I` is the radiant intensity,
  - `r` is the distance from the source,
  - `θ` is the angle of incidence.

This formulation highlights the dependency of radiance on both the distance from the light source and the angle of incidence.

## 5. Relation to Other Quantities

### 5.1 Radiant Intensity

Radiant intensity `I` measures the radiant power emitted by a source in a particular direction, but unlike radiance, it does not take into account the area over which the light is emitted. The relationship between radiance and intensity is given by:

- **Formula**: `L = I / (A cos(θ))`

Radiance essentially represents how the intensity is distributed over the projected area of the emitting surface.

### 5.2 Irradiance

Irradiance `E` measures the total radiant flux received by a surface, without considering the directionality of the incoming light. Radiance, on the other hand, describes the directional distribution of that light. 

- **Formula**: `E = ∫L cos(θ) dω`
  
  Here, irradiance can be calculated by integrating the radiance over all incoming directions.

## 6. Physical Interpretation

Radiance provides a detailed description of how light is distributed across a scene and how it interacts with surfaces. It is often used in computer graphics, vision, and lighting simulations to determine how objects will appear when illuminated by different light sources.

For example, radiance helps explain why some parts of a surface appear brighter or darker based on their angle relative to a light source and the observer. In photography, radiance is key to understanding how light intensity varies across the image and how much light is captured by the camera sensor in different parts of the scene.

## 7. Formula Breakdown

### 7.1 Surface Radiance

- **Formula**: `L = d²Φ / (dA · cos(θ) · dω)`
  
  - `L` is the radiance or the amount of power per unit area, per unit solid angle,
  - `d²Φ` is the differential radiant flux passing through the surface,
  - `dA` is the differential surface area,
  - `cos(θ)` accounts for the angle of incidence,
  - `dω` is the solid angle in steradians.

### 7.2 Relation to Solid Angle and Radiant Intensity

- **Formula**: `L = (I / r²) cos(θ)`

Where `I` is the radiant intensity and `r` is the distance from the source.

## 8. Practical Applications

### 8.1 Computer Graphics and Rendering

In computer graphics, radiance is used to model how light interacts with objects in a scene. Accurate rendering of scenes depends on precise calculations of radiance to simulate the appearance of materials, reflections, and shading.

### 8.2 Photography and Imaging

In photography, radiance defines how much light from different parts of a scene reaches the camera sensor, influencing exposure, contrast, and brightness across the image. High radiance values correspond to bright areas, while low radiance values correspond to darker regions.

## 9. Formula Recap

### 9.1 Surface Radiance

- **Formula**: `L = d²Φ / (dA · cos(θ) · dω)`
- **Alternative Formula**: `L = (I / r²) cos(θ)`
- **Units**: Watts per square meter per steradian (`W/m²·sr`)
- **Description**: Radiance describes the radiant power emitted, reflected, transmitted, or received by a surface per unit area and per unit solid angle, in a specific direction.

## 10. Real-World Factors Affecting Radiance

Several factors can influence the observed radiance of a surface:

- **Surface material**: Some surfaces reflect more light than others.
- **Angle of incidence**: The angle between the light source and the surface affects the amount of light reaching or leaving the surface.
- **Distance**: As the distance from the light source increases, radiance decreases according to the inverse square law (`1/r²`).
- **Surrounding environment**: Objects in the environment can reflect or scatter light, altering the radiance observed on a surface.