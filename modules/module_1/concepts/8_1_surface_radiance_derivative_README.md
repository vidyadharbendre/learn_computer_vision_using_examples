# Surface Radiance Derivation

## Introduction

**Radiance** is a key concept in radiometry that describes the energy emitted, reflected, or transmitted by a surface in a specific direction, per unit solid angle, and per unit area. In this document, we will derive the formula for surface radiance step by step, where **J** will represent the radiant intensity, previously denoted as **I**.

## 1. Definition of Radiance

Radiance \(L(θ, φ)\) is the energy passing through a unit area of a surface in a specific direction, within a unit solid angle. It is essentially the flux per unit solid angle and per unit projected surface area.

Radiance is denoted as:

'L = \frac{d^2 \Phi}{dA \cdot dΩ \cdot \cos(θ)}'

Where:
- 'd^2 Φ' is the differential radiant flux (in watts).
- 'dA' is the differential surface area (in meters squared, m²).
- 'dΩ' is the differential solid angle (in steradians, sr).
- 'θ' is the angle between the surface normal and the direction of the radiation.
- '\cos(θ)' accounts for the projection of the surface area along the direction of the radiation.

Now, let's go step by step to derive this formula.

## 2. Radiant Flux \( \Phi \)

The total **radiant flux \( \Phi \)** is the total power emitted, transferred, or received in the form of electromagnetic radiation. The flux emitted by a source within a solid angle \(dΩ\) is given by:

'dΦ = J \cdot dΩ'

Where:
- 'dΦ' is the differential radiant flux (in watts, W).
- 'J' is the radiant intensity (in watts per steradian, W/sr).
- 'dΩ' is the differential solid angle (in steradians, sr).

### 2.1 Solid Angle \( dΩ \)

For a small surface area \( dA \) located at a distance \( r \) from the source, the solid angle subtended by that surface area is:

'dΩ = \frac{dA \cdot \cos(θ)}{r^2}'

Where:
- 'dA' is the surface area (in m²).
- '\cos(θ)' is the angle between the direction of the radiation and the surface normal.
- 'r' is the distance between the surface and the source.

### 2.2 Relationship Between Radiant Flux and Surface Area

Now, substituting the expression for 'dΩ' into the expression for 'dΦ':

'dΦ = J \cdot \frac{dA \cdot \cos(θ)}{r^2}'

Thus, the radiant flux through the surface area \( dA \) is proportional to the radiant intensity, the surface area, and the angle \( θ \).

## 3. Differential Radiant Flux \( d^2 \Phi \)

When we want to find the radiant flux per unit solid angle and per unit surface area, we take the second differential of the flux. This brings us to:

'd^2 \Phi = J \cdot \frac{dA \cdot \cos(θ)}{r^2}'

Here:
- 'd^2 \Phi' represents the **differential radiant flux** emitted within a solid angle and a differential surface area.

## 4. Surface Radiance \( L(θ, φ) \)

Radiance is defined as the differential flux per unit projected area, per unit solid angle. Rearranging the above formula to express radiance:

'L(θ, φ) = \frac{d^2 \Phi}{dA \cdot dΩ \cdot \cos(θ)}'

Where:
- 'L(θ, φ)' is the radiance as a function of the angles \( θ \) and \( φ \).
- '\cos(θ)' adjusts for the projection of the surface relative to the direction of the radiation.

## 5. Summary

The surface radiance formula provides the relationship between the radiant intensity, the surface area, and the solid angle through which the energy is radiated. The key steps in the derivation involve understanding how radiant flux is related to the solid angle and surface area. The final radiance formula is:

'L = \frac{d^2 \Phi}{dA \cdot dΩ \cdot \cos(θ)}'

This equation allows us to calculate the radiance for any given direction of radiation relative to the surface.
