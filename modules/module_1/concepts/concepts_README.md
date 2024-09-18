# Concepts in Computer Vision

## 1. **Angle in 2 Dimensions**

### a) **Definition**
   In a 2D coordinate system, an angle is measured between two lines or vectors originating from a common point (usually the origin). The angle is typically measured in radians.

### b) **Radians**
   - **Description**: A radian is the angle subtended by an arc of a circle where the length of the arc is equal to the radius of the circle. One radian equals approximately 57.2958 degrees.
   - **Formula**: If \( \theta \) is the angle in radians, it can be computed using the arc length \( dL \) and the radius \( r \) of the circle:
     <p align="center">
     θ = dL / r
     </p>
   - **Example**: An angle of 90 degrees is equivalent to &pi;/2 radians.

### c) **Differential Arc Length**
   - **Formula**: For a small differential angle \( d\theta \), the differential arc length \( dL \) is:
     <p align="center">
     dL = r * dθ
     </p>
   - **Explanation**: In this formula, \( dL \) represents a small segment of the arc on the circle, \( r \) is the radius, and \( dθ \) is the small angle in radians.

### d) **Applications**
   - **Rotation**: Rotating a 2D object around the origin involves specifying an angle in radians.
   - **Trigonometry**: Used in trigonometric functions such as sine, cosine, and tangent to calculate positions and distances.

### e) **Reference**
   - **Text**: *Mathematics for 2D and 3D Graphics* - J. Allaire and M. Papalaskari (2010)

## 2. **Angle in 3 Dimensions**

### a) **Definition**
   In a 3D coordinate system, an angle can be defined between two vectors or planes. The angle can be described using various methods including the dot product, rotation matrices, or Euler angles.

### b) **Radians**
   - **Description**: Similar to 2D, a radian in 3D is the angle subtended by an arc on a sphere where the arc length is equal to the radius of the sphere.
   - **Formula**: For two vectors <i>u</i> and <i>v</i> with the dot product <i>u · v</i>, the angle <i>θ</i> between them is:
     <p align="center">
     θ = arccos((<i>u · v</i>) / (|<i>u</i>| · |<i>v</i>|))
     </p>
   - **Example**: The angle between two vectors in 3D space can be computed using the dot product formula, providing a measure of how aligned or opposed the vectors are.

### c) **Applications**
   - **Rotation**: Used in 3D graphics and computer vision to describe the orientation of objects and camera angles.
   - **Transformation**: Essential for modeling and rendering 3D objects, including rotations and translations.

### d) **Reference**
   - **Text**: *3D Math Primer for Graphics and Game Development* - E. G. Schreier (2010)

## 3. **Comparative Overview**

### a) **2D Angles**
   - **Characteristics**: Simple and direct measurement, applicable to flat surfaces and rotations in a plane.
   - **Usage**: Basic graphics, planar geometry, simple rotations.

### b) **3D Angles**
   - **Characteristics**: More complex due to additional dimension, involves vectors and matrices for computation.
   - **Usage**: Advanced graphics, spatial transformations, robotics.

## 4. **Differential Solid Angle in Spherical Coordinates**

### a) **Formula**
   - **Description**: The differential element of a solid angle in spherical coordinates can be expressed as:
     <p align="center">
     dw = (dA * cos(θ)) / r²
     </p>

### b) **Explanation**
   - **dw**: Differential solid angle.
   - **dA**: Differential area element on the surface.
   - **θ**: Angle between the surface normal and the observation direction.
   - **r**: Radial distance from the origin.

   **Note**: This formula shows how the solid angle (dw) is influenced by the differential area (dA) and the radial distance squared (r²). The cosine term adjusts for the angle between the surface normal and the observation direction.

### c) **Applications**
   - **Radiometry**: Calculating radiance and flux in optics and computer vision.
   - **3D Modeling**: Helps in determining visibility and light interaction with surfaces.

---

For additional reading and in-depth understanding of these concepts, refer to the provided textbooks and online resources.