# Image Irradiance

## Introduction

**Image Irradiance** refers to the amount of radiant flux (light energy) that reaches a unit area of the image plane in a camera or imaging system. This concept is fundamental in computer vision, image formation, and radiometry. It directly relates to the brightness of the pixels in the final image and is influenced by the radiance of the scene and the optical properties of the camera.

## 1. Definition

**Image Irradiance (E_image)** is the measure of how much radiant energy reaches a unit area of the image plane.

- **Unit**: Watts per square meter (`W/m²`)
- **Formula**: `E_image = L_scene * (cos(θ) / r²)`
  
  where:
  - `E_image` is the image irradiance,
  - `L_scene` is the scene radiance,
  - `θ` is the angle between the surface normal and the incident light direction,
  - `r` is the distance between the surface and the image plane.

Image irradiance depends on the scene radiance, the camera's distance from the scene, and the angle at which light hits the camera sensor.

## 2. Factors Affecting Image Irradiance

### 2.1 Scene Radiance

The primary factor influencing **image irradiance** is the **scene radiance**. The more radiant energy emitted or reflected by objects in the scene, the higher the irradiance that reaches the camera's sensor.

- **Formula**: `E_image = L_scene * (cos(θ) / r²)`

This relationship shows that image irradiance is proportional to the scene radiance.

### 2.2 Angle of Incident Light (cos θ)

The **angle of incidence** also plays a critical role. Light striking the image sensor at a more perpendicular angle (i.e., smaller θ) results in higher irradiance.

- **Formula**: `E_image = L_scene * (cos(θ) / r²)`

If `θ = 0`, meaning the light is incident normally to the sensor, the irradiance is maximized.

### 2.3 Distance from the Scene (r²)

The irradiance is inversely proportional to the square of the distance between the camera and the scene. The farther the camera is from the scene, the lower the irradiance reaching the image plane.

- **Formula**: `E_image = L_scene * (cos(θ) / r²)`

This is consistent with the **inverse square law**, which states that the intensity of light decreases with the square of the distance from the source.

## 3. Image Formation Process

The irradiance that reaches the camera's image sensor determines the **brightness** or **intensity** of the pixels in the final image. The relationship between the irradiance on the image plane and the pixel values is typically modeled by a function that includes sensor characteristics such as quantum efficiency and exposure settings.

### 3.1 Image Intensity

The **image intensity** is proportional to the irradiance at each point on the image plane. Each pixel's brightness in the image is directly related to the amount of irradiance it receives.

- **Formula**: `I(x, y) ∝ E_image`

  where:
  - `I(x, y)` is the image intensity at pixel `(x, y)`,
  - `E_image` is the irradiance at the corresponding point on the image plane.

## 4. Formula for Image Irradiance

### 4.1 Standard Image Irradiance Formula

- **Formula**: `E_image = L_scene * (cos(θ) / r²)`
  
  where:
  - `E_image` is the image irradiance,
  - `L_scene` is the scene radiance,
  - `θ` is the angle of incident light,
  - `r` is the distance from the scene.

### 4.2 Image Intensity

Image intensity can be computed based on the irradiance at each point on the image plane:

- **Formula**: `I(x, y) ∝ E_image`

The image irradiance defines the pixel brightness values in the image.

## 5. Relation to Scene Radiance

**Image Irradiance** is directly related to **scene radiance**. Scene radiance (`L_scene`) describes the light emitted or reflected by the objects in the scene, while image irradiance (`E_image`) quantifies how much of that light reaches the image plane.

- **Formula**: `E_image = L_scene * (cos(θ) / r²)`

The scene radiance is the driving factor behind the amount of light reaching the camera and thus influences the resulting pixel intensities.

## 6. Practical Applications

### 6.1 Computer Vision and Image Processing

In **computer vision**, understanding image irradiance is crucial for accurately interpreting image data. Variations in irradiance due to scene lighting conditions, surface properties, and camera positioning affect the appearance of objects in the image, impacting tasks like object detection, 3D reconstruction, and image segmentation.

### 6.2 Photography and Imaging

In **photography**, controlling image irradiance through exposure settings, lighting, and camera distance is essential for achieving the desired brightness and contrast in images. Image irradiance also affects **dynamic range** and **sensor noise**.

### 6.3 Remote Sensing

In **remote sensing**, irradiance plays a vital role in interpreting satellite and aerial imagery. The irradiance detected by the sensor helps in understanding surface properties, atmospheric effects, and environmental conditions.

## 7. Physical Interpretation

### 7.1 Brightness and Exposure

Image irradiance influences the **brightness** of each pixel in an image. The exposure settings of a camera, such as aperture, shutter speed, and ISO, modulate how much irradiance is captured by the sensor, affecting the final image's brightness.

### 7.2 Light Distribution Across the Scene

Different parts of the scene may emit or reflect varying amounts of light, resulting in spatial variations in irradiance across the image plane. These variations create the light and dark regions of an image, corresponding to areas of high and low radiance in the scene.

## 8. Formula Breakdown

### 8.1 Image Irradiance Formula

- **Formula**: `E_image = L_scene * (cos(θ) / r²)`
  
  where:
  - `E_image` is the image irradiance,
  - `L_scene` is the scene radiance,
  - `θ` is the angle between the surface normal and the incident light,
  - `r` is the distance from the surface to the image plane.

### 8.2 Image Intensity Formula

- **Formula**: `I(x, y) ∝ E_image`
  
  This expresses the image intensity at each pixel as proportional to the irradiance at the corresponding point on the image plane.

## 9. Real-World Factors Affecting Image Irradiance

Several factors influence **image irradiance** and thus the appearance of images:

- **Surface Properties**: Different materials reflect or emit light differently, affecting the irradiance at the image plane.
- **Lighting Conditions**: The intensity, direction, and type of light sources in the scene determine the amount of light reaching the camera.
- **Camera Settings**: The aperture, focal length, and sensor characteristics control how much light is captured, influencing the image irradiance.
- **Distance from the Scene**: As the camera moves farther from the scene, the irradiance decreases due to the inverse square law.

## 10. Formula Recap

### 10.1 Image Irradiance Formula

- **Formula**: `E_image = L_scene * (cos(θ) / r²)`
  
  where:
  - `E_image` is the image irradiance,
  - `L_scene` is the scene radiance,
  - `θ` is the angle of incidence,
  - `r` is the distance from the scene to the image plane.

### 10.2 Image Intensity Formula

- **Formula**: `I(x, y) ∝ E_image`
  
  This expresses the proportional relationship between image intensity and image irradiance.
