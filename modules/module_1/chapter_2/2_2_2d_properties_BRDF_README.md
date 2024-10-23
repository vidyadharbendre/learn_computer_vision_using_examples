# Properties of BRDF (Bidirectional Reflectance Distribution Function)

The BRDF describes how light is reflected at an opaque surface. It is a 4-dimensional function that defines how light is scattered from the incident direction to the outgoing direction. Below are the key properties of BRDF.

## 1. Non-Negative: 'f(θᵢ, φᵢ; θᵣ, φᵣ) ≥ 0'

- **Definition**: The BRDF function is always non-negative for all angles of incident and outgoing directions. The reflectance cannot be negative, meaning the amount of light reflected is always either zero or positive.
  
- **Mathematical Representation**: For any incoming and outgoing directions, the BRDF satisfies:
  
  'f(θᵢ, φᵢ; θᵣ, φᵣ) ≥ 0'

## 2. Helmholtz Reciprocity

- **Definition**: The BRDF obeys **Helmholtz reciprocity**, meaning the function is symmetric when the incident and reflected directions are swapped. This ensures that the path of light between two points can be reversed without affecting the amount of reflected light.

- **Mathematical Representation**:

  'f(θᵢ, φᵢ; θᵣ, φᵣ) = f(θᵣ, φᵣ; θᵢ, φᵢ)'

  where:
  - '(θᵢ, φᵢ)' are the incident angles,
  - '(θᵣ, φᵣ)' are the reflected angles.

## 3. 4-Dimensional Function

- **Definition**: The BRDF is a **4-dimensional function**, as it depends on two directions: the incident light direction and the reflected light direction, each described by two angles (θ and φ). These angles include both the azimuth and zenith for the incoming and outgoing light.

- **Mathematical Representation**:

  'f(θᵢ, φᵢ; θᵣ, φᵣ)'

  where:
  - 'θᵢ' and 'φᵢ' are the incident zenith and azimuth angles,
  - 'θᵣ' and 'φᵣ' are the reflected zenith and azimuth angles.

## 4. Rotationally Symmetric

- **Definition**: A **rotationally symmetric** BRDF is one where the reflectance depends only on the relative angle between the incident and reflected directions, not on their absolute orientations. This simplifies the BRDF to fewer parameters when symmetry exists.

- **Mathematical Representation**:

  If the BRDF is rotationally symmetric, it can be simplified as:

  'f(θᵢ, θᵣ, |φᵢ - φᵣ|)'
