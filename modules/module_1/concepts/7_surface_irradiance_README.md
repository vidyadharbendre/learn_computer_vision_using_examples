# Surface Irradiance

## Introduction

**Surface Irradiance** is a radiometric measure that describes the power of electromagnetic radiation (light) incident on a surface, per unit area. It plays a key role in understanding how much light energy is received by a surface, and it is used in fields like solar energy, lighting, and climate science.

## 1. Definition

**Irradiance (E)** is defined as the amount of radiant flux (`Φ`) received by a surface per unit area (`A`). It is essentially a measure of how much energy hits a particular area of a surface from a light source.

- **Unit**: Watts per square meter (`W/m²`)
- **Formula**: `E = dΦ / dA`
  
  where:
  - `E` is the irradiance,
  - `dΦ` is the differential radiant flux,
  - `dA` is the differential area.

## 2. Extended Formula

In cases where the radiation is not perpendicular to the surface, we can extend the formula to account for the angle of incidence (`θ`). This is important because the effective area receiving light decreases as the angle of incidence increases.

The extended formula incorporates the angle `θ` between the incoming light and the surface normal:

- **Extended Formula**: `E = (dΦ / dA) cos(θ) / r²`
  
  where:
  - `E` is the irradiance,
  - `dΦ` is the differential radiant flux,
  - `dA` is the surface area,
  - `θ` is the angle of incidence,
  - `r` is the distance from the source.

## 3. Formula with Solid Angle

Another way to express irradiance is using the concept of **solid angle (dω)**. The solid angle subtended by a differential area `dA` can be used to relate irradiance to radiance.

- **Formula**: `E = J \cdot dω / dA`
  
  where:
  - `E` is the irradiance,
  - `J` is the radiance (or directional flux),
  - `dω` is the solid angle,
  - `dA` is the differential area.

In this form, irradiance is the product of the radiance and the solid angle subtended by the surface.

### 3.1 Connection to Radiance

The radiance `J` describes the amount of light emitted by a source in a given direction, and by multiplying it by the solid angle per unit area (`dω / dA`), we get the surface irradiance.

- **Substitution**: `dA cos(θ) / r² = J cos(θ) / r²`
  
This ties the irradiance to the directional properties of the radiance and the geometric factors such as angle and distance.

## 4. Types of Irradiance

### 4.1 Direct Irradiance

**Direct Irradiance** refers to the radiation that hits the surface directly from a light source, without being scattered or diffused. For example, sunlight that reaches the ground without being affected by clouds or particles in the atmosphere is direct irradiance.

### 4.2 Diffuse Irradiance

**Diffuse Irradiance** comes from radiation that has been scattered in the atmosphere. This is the light that still reaches a surface, but not directly from the light source. On cloudy days, most of the sunlight reaching the ground is diffuse.

### 4.3 Global Irradiance

**Global Irradiance** is the total irradiance received by a surface, consisting of both direct and diffuse components.

## 5. Physical Interpretation

Irradiance represents how much radiant energy is hitting a given area on a surface. For example, the **irradiance of sunlight** on a solar panel can be used to calculate how much power the panel can generate. Higher irradiance means more energy is available for conversion to electricity.

## 6. Formula Breakdown

- **Surface Irradiance**: `E = dΦ / dA`
  
  - `E` represents the irradiance, or power per unit area,
  - `dΦ` is the radiant flux (power) received by the surface,
  - `dA` is the surface area over which the flux is distributed.

When factoring in the angle `θ` and distance `r` from the source:

- **Extended Formula**: `E = (J cos(θ)) / r²`

Where `J` represents the directional flux (or radiance) emitted by the source, distributed over the surface area adjusted for angle and distance.


- **Example**

If a surface receives **100 W** of radiant flux spread over an area of **2 m²**, the irradiance is:

`E = 100 W / 2 m² = 50 W/m²`

This means the surface is receiving 50 watts of power per square meter.


### 6.1 Alternative Formula Using Solid Angle

Another expression of irradiance relates to the solid angle `dω` subtended by the surface:

- **Formula**: `E = J \cdot dω / dA`
  
This relationship connects the radiance with the solid angle projected onto the surface.

## 7. Application in Solar Energy

In solar energy systems, **irradiance** is used to determine how much solar power is available for conversion into electricity. Solar panels are typically rated based on the amount of irradiance they receive (in `W/m²`). Higher irradiance results in more electrical output from a solar panel.

## 8. Formula Recap

### 8.1 Surface Irradiance

- **Formula**: `E = dΦ / dA`
- **Extended Formula**: `E = (J cos(θ)) / r²`
- **Alternative Formula**: `E = J \cdot dω / dA`
- **Units**: Watts per square meter (`W/m²`)
- **Description**: The amount of radiant energy hitting a surface per unit area.

## 9. Practical Considerations

### Measuring Irradiance

Irradiance can be measured using devices like **pyranometers**, which are used to assess the total energy received from sunlight in applications such as weather monitoring, solar panel optimization, and climate studies.

### Real-World Factors

In practice, surface irradiance depends on:
- **Time of day**: Higher irradiance at midday compared to morning or evening.
- **Weather conditions**: Clouds can significantly reduce direct irradiance, but diffuse irradiance still reaches the ground.
- **Surface orientation**: Surfaces perpendicular to the incoming light receive higher irradiance than slanted surfaces.


