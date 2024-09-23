# Image Intensity

## Introduction

**Image Intensity** refers to the brightness or lightness of a pixel in an image. It represents the amount of light that has reached the camera sensor and is recorded as a digital value in the image. The intensity value of each pixel is determined by the **image irradiance**, which in turn depends on the radiance of the scene and the camera's optical system. In grayscale images, the intensity is usually a single value, while in color images, it corresponds to the combination of **Red (R)**, **Green (G)**, and **Blue (B)** color channels.

## 1. Definition

**Image Intensity (I)** describes the level of brightness for each pixel in an image. It is directly proportional to the irradiance received by the camera sensor at that point.

- **Unit**: Typically an 8-bit integer (ranging from 0 to 255 in most imaging systems), but can also be expressed as a floating-point value depending on the system's bit depth.
- **Formula**: `I(x, y) ∝ E_image`
  
  where:
  - `I(x, y)` is the intensity at pixel `(x, y)`,
  - `E_image` is the image irradiance at that point.

In digital images, **intensity** can represent a range of brightness levels, with 0 representing black and higher values representing brighter pixels.

## 2. Factors Affecting Image Intensity

### 2.1 Image Irradiance

The intensity of each pixel is proportional to the **image irradiance** at the corresponding point in the image plane. Higher irradiance leads to higher pixel intensity.

- **Formula**: `I(x, y) ∝ E_image`

### 2.2 Scene Radiance

The **scene radiance (L_scene)** determines how much light is emitted or reflected by objects in the scene and contributes to the **image irradiance**. This, in turn, affects the pixel intensity.

- **Formula**: `E_image = L_scene * (cos(θ) / r²)`
  
  where:
  - `L_scene` is the radiance of the scene,
  - `θ` is the angle between the surface normal and the direction of the incoming light,
  - `r` is the distance from the surface to the image plane.

### 2.3 Distance from the Scene

The **distance from the scene (r)** impacts the intensity because the image irradiance follows the **inverse square law**. As the distance between the camera and the scene increases, the intensity decreases.

- **Formula**: `I(x, y) ∝ L_scene * (cos(θ) / r²)`

### 2.4 Camera Response Function

The intensity recorded in the image is also affected by the **camera response function**, which maps the irradiance into a pixel value. This response is often nonlinear and can be adjusted based on camera settings like **exposure** and **ISO**.

## 3. Image Intensity in Grayscale and Color Images

### 3.1 Grayscale Images

In **grayscale images**, the intensity value at each pixel is a single number representing the brightness.

- **Range**: [0, 255] (for 8-bit images)
  - 0 represents black,
  - 255 represents white.

### 3.2 Color Images

In **color images**, the intensity at each pixel is a combination of three values: **Red (R)**, **Green (G)**, and **Blue (B)**, often represented in hexadecimal format as `#RRGGBB`.

- **Example**: For a pixel with intensity represented by the hexadecimal code `#FFA07A`, the intensity values for the red, green, and blue channels are:
  - **Red**: FF (255 in decimal),
  - **Green**: A0 (160 in decimal),
  - **Blue**: 7A (122 in decimal).

## 4. Image Intensity Formula

### 4.1 Intensity Proportional to Irradiance

- **Formula**: `I(x, y) ∝ E_image`
  
  where:
  - `I(x, y)` is the pixel intensity at location `(x, y)`,
  - `E_image` is the irradiance at that point on the image plane.

### 4.2 Intensity in Terms of Scene Radiance

The relationship between **scene radiance** and **image intensity** can be expressed as:

- **Formula**: `I(x, y) ∝ L_scene * (cos(θ) / r²)`
  
  where:
  - `L_scene` is the scene radiance,
  - `θ` is the angle of incidence,
  - `r` is the distance from the scene to the image plane.

## 5. Practical Applications

### 5.1 Computer Vision

In **computer vision**, **image intensity** is a key feature for tasks such as **edge detection**, **segmentation**, and **object recognition**. The intensity patterns in an image help algorithms interpret the structure and content of the scene.

### 5.2 Photography and Image Processing

In **photography**, controlling **image intensity** through exposure, lighting, and post-processing can dramatically affect the mood and appearance of an image.

### 5.3 Medical Imaging

In **medical imaging**, intensity levels in grayscale images, such as X-rays or MRIs, represent varying densities of tissues, which are crucial for diagnosis.

## 6. Brightness Adjustment Techniques

Adjusting **image intensity** is a common operation in image processing. Here are some basic techniques:

### 6.1 Gamma Correction

Gamma correction adjusts the brightness of an image by applying a power-law relationship between the input and output intensity values.

- **Formula**: `I_out = I_in^γ`
  
  where:
  - `I_in` is the input intensity,
  - `γ` is the gamma value,
  - `I_out` is the output intensity after gamma correction.

### 6.2 Histogram Equalization

**Histogram equalization** improves the contrast of an image by redistributing the intensity values to cover a wider range.

## 7. Formula Breakdown

### 7.1 Image Intensity Formula

- **Formula**: `I(x, y) ∝ E_image`
  
  where:
  - `I(x, y)` is the intensity at pixel `(x, y)`,
  - `E_image` is the irradiance at that point on the image plane.

### 7.2 Image Intensity in Terms of Scene Radiance

- **Formula**: `I(x, y) ∝ L_scene * (cos(θ) / r²)`
  
  where:
  - `L_scene` is the scene radiance,
  - `θ` is the angle between the surface normal and the incident light,
  - `r` is the distance from the scene to the image plane.

## 8. Real-World Factors Affecting Image Intensity

### 8.1 Exposure Settings

**Exposure settings** such as shutter speed, aperture, and ISO sensitivity directly affect the image intensity. Longer exposure times and wider apertures allow more light to reach the sensor, increasing intensity.

### 8.2 Lighting Conditions

The intensity of light sources in the scene determines how much irradiance reaches the camera sensor, influencing pixel brightness.

### 8.3 Surface Reflectivity

**Reflective surfaces** can create bright spots in images due to their higher radiance, resulting in higher pixel intensity.

## 9. Formula Recap

### 9.1 Intensity Proportional to Irradiance

- **Formula**: `I(x, y) ∝ E_image`
  
  where:
  - `I(x, y)` is the pixel intensity at location `(x, y)`,
  - `E_image` is the irradiance at that point.

### 9.2 Intensity in Terms of Scene Radiance

- **Formula**: `I(x, y) ∝ L_scene * (cos(θ) / r²)`
  
  This formula links image intensity to the scene radiance, taking into account the angle of incidence and the distance from the scene.

