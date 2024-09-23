# Scene Radiance

## Introduction

**Scene Radiance** refers to the total radiance observed in a scene, encompassing all the light reflected, emitted, or transmitted by objects within the scene that reach the observer or camera. It combines the radiance contributions from various surfaces, light sources, and environmental factors to determine how light is distributed throughout the scene and how it appears to a viewer or imaging device.

## 1. Definition

**Scene Radiance (L_scene)** describes the cumulative radiance across an entire scene. This includes contributions from multiple surfaces, reflections, and different angles of light entering the camera or the observer's eyes.

- **Unit**: Watts per square meter per steradian (`W/m²·sr`)
- **Formula**: `L_scene = Σ L_surface_i`
  
  where:
  - `L_scene` is the scene radiance,
  - `L_surface_i` is the radiance from the `i`-th surface in the scene.

Scene radiance is essentially the sum of radiance values from all visible surfaces in a scene, integrated over the entire image plane.

## 2. Components of Scene Radiance

### 2.1 Surface Contributions

Each surface in the scene contributes to the overall radiance. The surface radiance (`L_surface`) from each object is influenced by factors such as material properties, the angle of incident light, and reflections. The total radiance for a scene is a combination of all these surface radiances.

- **Formula**: `L_scene = Σ L_surface_i`
  
  This indicates that the overall scene radiance is a sum of all individual surface radiances.

### 2.2 Environmental Lighting

Apart from direct surface contributions, **environmental lighting** such as ambient light, reflections from surrounding objects, and even light scattered by the atmosphere contributes to the scene radiance. This indirect lighting plays a critical role in the overall appearance of the scene.

## 3. Scene Radiance as a Cumulative Quantity

Scene radiance is a **cumulative** radiometric quantity. It accounts for the total amount of light from all directions, surfaces, and sources that make up the visual impression of the scene. As opposed to **surface radiance**, which focuses on a single point on an object, scene radiance evaluates the entire scene's radiance at various points.

- **Directional Dependency**: Like surface radiance, scene radiance depends on the direction from which light reaches the camera or observer. As different surfaces reflect light at various angles, the scene radiance varies across the image plane.

## 4. Formula for Scene Radiance

### 4.1 Standard Scene Radiance Formula

The scene radiance can be computed by summing the radiance values of all visible surfaces in the scene:

- **Formula**: `L_scene = Σ L_surface_i`
  
  where:
  - `L_scene` is the total scene radiance,
  - `L_surface_i` is the radiance of the `i`-th surface in the scene.

### 4.2 Scene Radiance Including Environmental Lighting

Considering both surface and environmental contributions, the formula becomes:

- **Formula**: `L_scene = Σ L_surface_i + L_env`

  where:
  - `L_surface_i` is the radiance from the `i`-th surface,
  - `L_env` represents the contribution from environmental lighting sources (ambient light, reflections, scattered light).

## 5. Relation to Surface Radiance

Scene radiance is directly related to **surface radiance** because each object or surface in the scene contributes to the overall radiance. While surface radiance focuses on the radiant power from a single surface, scene radiance aggregates the radiance contributions from multiple surfaces, objects, and directions.

- **Formula**: `L_scene = Σ L_surface_i`

This shows that scene radiance is essentially a summation of surface radiances across all objects visible in the scene.

## 6. Physical Interpretation

Scene radiance explains the total light distribution in a visual environment. It is critical in applications like imaging, rendering, and computer vision, where understanding how light interacts with multiple objects and surfaces within a scene is essential.

### 6.1 Image Formation

In photography and imaging, **scene radiance** determines the amount of light that reaches the camera sensor from each part of the scene. The sensor captures the cumulative radiance at each pixel, producing the final image. Higher scene radiance corresponds to brighter areas in the image, while lower scene radiance results in darker regions.

### 6.2 Reflections and Shadows

Scene radiance also accounts for **reflections** and **shadows** in the scene. Reflections from shiny surfaces and shadows created by objects blocking light contribute to the overall radiance observed by the camera. These effects are essential for understanding the appearance of objects in realistic lighting conditions.

## 7. Practical Applications

### 7.1 Computer Graphics and Rendering

In computer graphics, **scene radiance** is a fundamental concept for rendering realistic images. By simulating how light interacts with surfaces and propagates through a scene, rendering algorithms calculate scene radiance to produce realistic lighting, reflections, and shadows.

### 7.2 Remote Sensing and Imaging

In remote sensing, **scene radiance** helps determine the amount of light reflected or emitted by the Earth's surface and atmosphere. This information is critical for interpreting satellite imagery, environmental monitoring, and climate studies.

### 7.3 Vision Systems

For autonomous systems, such as self-driving cars and drones, **scene radiance** is used to evaluate the visual environment and detect objects, obstacles, and relevant features.

## 8. Formula Breakdown

### 8.1 Scene Radiance Formula

- **Formula**: `L_scene = Σ L_surface_i`
  
  where:
  - `L_scene` is the total scene radiance,
  - `L_surface_i` is the radiance from the `i`-th surface.

### 8.2 Scene Radiance with Environmental Contributions

- **Formula**: `L_scene = Σ L_surface_i + L_env`
  
  where:
  - `L_scene` is the total radiance in the scene,
  - `L_surface_i` is the surface radiance from the `i`-th surface,
  - `L_env` is the radiance contribution from environmental sources.

### 8.3 Radiance at a Single Point

The radiance at a single point in the scene from a surface can be given by:

- **Formula**: `L_surface = d²Φ / (dA · cos(θ) · dω)`
  
  where:
  - `L_surface` is the radiance from the surface,
  - `d²Φ` is the differential radiant flux,
  - `dA` is the differential surface area,
  - `θ` is the angle between the surface normal and the incident light,
  - `dω` is the solid angle.

## 9. Real-World Factors Affecting Scene Radiance

Several factors can influence the observed scene radiance:

- **Surface Materials**: Different surfaces reflect or emit light differently, impacting the total radiance in the scene.
- **Lighting Conditions**: The intensity, direction, and type of light sources in the environment significantly affect the scene radiance.
- **Viewing Angle**: The angle at which the camera or observer views the scene can affect how much radiance is captured from each surface.
- **Environmental Lighting**: Indirect lighting, such as ambient light and reflections from other surfaces, also contributes to the scene radiance.

## 10. Formula Recap

### 10.1 Scene Radiance

- **Formula**: `L_scene = Σ L_surface_i`
  
  where:
  - `L_scene` is the total scene radiance,
  - `L_surface_i` is the radiance from each surface in the scene.

### 10.2 Scene Radiance with Environmental Contributions

- **Formula**: `L_scene = Σ L_surface_i + L_env`
  
  This incorporates both surface radiance and environmental lighting effects.

### 10.3 Single Surface Radiance

- **Formula**: `L_surface = d²Φ / (dA · cos(θ) · dω)`
  
  This formula explains the radiance from a single surface within the scene.
