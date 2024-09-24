# Surface Radiance Derivation

## Introduction

Radiance is an important concept in radiometry that defines the **amount of energy** emitted, reflected, or transmitted from a surface in a specific direction, per unit solid angle. This document walks through the step-by-step derivation of the surface radiance formula.

## 1. Definition of Radiance

**Radiance** \(L\) is mathematically defined as the energy passing through a unit area in a specific direction per unit solid angle:

\[
L(θ, φ) = \frac{d²Φ}{dA \cdot dΩ \cdot \cos(θ)}
\]

Where:
- \(L(θ, φ)\) is the radiance for angles \(θ\) (zenith) and \(φ\) (azimuth).
- \(d²Φ\) is the differential radiant flux.
- \(dA\) is the differential area.
- \(dΩ\) is the differential solid angle.
- \(\cos(θ)\) accounts for the angle of the surface relative to the direction of interest.

## 2. Derivation Steps

### Step 1: Consider a Radiating Surface

Let’s consider a surface that emits radiant energy uniformly in all directions.

### Step 2: Define Differential Areas and Angles

Assume a differential area \(dA\) on the surface and a solid angle \(dΩ\) into which the energy is emitted.

### Step 3: Relate Radiant Flux to Radiance

From the definition of radiance, we can express the differential radiant flux \(d²Φ\) in terms of radiance as follows:

\[
d²Φ = L(θ, φ) \cdot dA \cdot dΩ \cdot \cos(θ)
\]

### Step 4: Deriving \(d²Φ\)

To understand how we derive \(d²Φ\), we start with the definition of **radiant flux** \(Φ\), which is the total power emitted, transferred, or received in the form of electromagnetic radiation. 

1. The radiant flux \(dΦ\) emitted into a solid angle \(dΩ\) is given by:

   \[
   dΦ = J \cdot dΩ
   \]

   Where:
   - \(dΦ\) is the differential radiant flux (in watts, W).
   - \(J\) is the radiant intensity (in watts per steradian, W/sr).
   - \(dΩ\) is the differential solid angle (in steradians, sr).

2. For a small surface area \(dA\) located at a distance \(r\) from the source, the solid angle \(dΩ\) subtended by that surface area can be expressed as:

   \[
   dΩ = \frac{dA \cdot \cos(θ)}{r^2}
   \]

   Where:
   - \(dA\) is the surface area (in m²).
   - \(\cos(θ)\) is the angle between the direction of the radiation and the surface normal.
   - \(r\) is the distance between the surface and the source.

3. Substituting the expression for \(dΩ\) into the expression for \(dΦ\), we get:

   \[
   dΦ = J \cdot \frac{dA \cdot \cos(θ)}{r^2}
   \]

4. Now, when we consider \(d²Φ\) as the radiant flux per unit solid angle and per unit surface area, we express this as:

   \[
   d²Φ = J \cdot dA \cdot \frac{\cos(θ)}{r^2}
   \]

### Step 5: Integrate Over the Surface and Solid Angle

To find the total radiant flux emitted by the surface, integrate over the solid angle and the surface area:

\[
Φ = \int\int L(θ, φ) \cdot dA \cdot dΩ \cdot \cos(θ)
\]

## 3. Example

An example of radiance could be:

>If a surface emits 10 W/m² in a specific direction within a solid angle of 0.1 sr, the surface radiance would be calculated accordingly.

## 4. Conclusion

Surface radiance is a key parameter in understanding how surfaces emit energy. By defining radiance in relation to differential areas and solid angles, we can derive useful formulas that apply in various fields of science and engineering.
