# BRDF - Bidirectional Reflectance Distribution Function

### What is BRDF?
- **Definition**: The **Bidirectional Reflectance Distribution Function (BRDF)** describes how light is reflected at an opaque surface.
- It defines the relationship between the **incoming light** direction and the **reflected light** direction from a surface.
- The BRDF is a **4-dimensional function** that takes in two sets of angles:
  - **Incoming direction**: Defined by angles `θ_i` (zenith angle) and `φ_i` (azimuth angle).
  - **Outgoing direction**: Defined by angles `θ_r` (zenith angle) and `φ_r` (azimuth angle).
  
### BRDF Notation
- Mathematically, BRDF is represented as:
  - `f_r(θ_i, φ_i, θ_r, φ_r)`
- It describes the ratio of **reflected radiance** to **incident irradiance** for a given pair of incoming and outgoing directions.

### Properties of BRDF:
1. **Reciprocity**: 
   - `f_r(θ_i, φ_i, θ_r, φ_r) = f_r(θ_r, φ_r, θ_i, φ_i)`
   - The function remains the same if you swap the incoming and outgoing directions.
   
2. **Energy Conservation**:
   - The reflected light cannot exceed the incident light. Therefore, the BRDF ensures that the total reflected radiance over all directions is less than or equal to the incoming radiance.

3. **Non-negativity**:
   - The BRDF must always be non-negative, meaning it cannot reflect a negative amount of light.

### Applications of BRDF:
- **Computer Graphics**: Used to simulate realistic surface reflections in rendering.
- **Remote Sensing**: Helps in understanding how light reflects off the Earth's surface for satellite imaging.
- **Optical Engineering**: Used in designing surfaces with specific reflective properties.

### Summary:
- The BRDF describes how light reflects from a surface based on the angle of incoming and outgoing light.
- It is a key function in fields that deal with light interaction with surfaces, helping simulate and analyze real-world reflections.
