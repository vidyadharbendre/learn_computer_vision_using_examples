# Surface Radiance Derivation

## Introduction

Radiance is an important concept in radiometry that defines the **amount of energy** emitted, reflected, or transmitted from a surface in a specific direction, per unit solid angle. This document walks through the step-by-step derivation of the surface radiance formula.

## 1. Definition of Radiance

**Radiance** \(L\) is mathematically defined as the energy passing through a unit area in a specific direction per unit solid angle:

'L(θ, φ) = d²Φ / (dA · dΩ · cos(θ))'

Where:
- \(L(θ, φ)\) is the radiance for angles \(θ\) (zenith) and \(φ\) (azimuth).
- \(d²Φ\) is the differential radiant flux.
- \(dA\) is the differential area.
- \(dΩ\) is the differential solid angle.
- \(cos(θ)\) accounts for the angle of the surface relative to the direction of interest.

## 2. Derivation Steps

### Step 1: Consider a Radiating Surface

Let’s consider a surface that emits radiant energy uniformly in all directions.

### Step 2: Define Differential Areas and Angles

Assume a differential area \(dA\) on the surface and a solid angle \(dΩ\) into which the energy is emitted.

### Step 3: Relate Radiant Flux to Radiance

From the definition of radiance, we can express the differential radiant flux \(d²Φ\) in terms of radiance as follows:

'd²Φ = L(θ, φ) · dA · dΩ · cos(θ)'

### Step 4: Integrate Over the Surface and Solid Angle

To find the total radiant flux emitted by the surface, integrate over the solid angle and the surface area:

'Φ = ∫∫ L(θ, φ) · dA · dΩ · cos(θ)'

## 3. Example

An example of radiance could be:

'If a surface emits 10 W/m² in a specific direction within a solid angle of 0.1 sr, the surface radiance would be calculated accordingly.'

## 4. Conclusion

Surface radiance is a key parameter in understanding how surfaces emit energy. By defining radiance in relation to differential areas and solid angles, we can derive useful formulas that apply in various fields of science and engineering.
