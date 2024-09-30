# Global Illumination

**Global Illumination** refers to the process of simulating how light interacts with all surfaces in a scene, not just direct lighting from a light source. This means that light can bounce off surfaces, reflect from one object to another, and even be absorbed, creating realistic lighting effects.

## Key Concepts of Global Illumination

- **Direct Illumination**: This is the light that comes straight from a light source to the object.
- **Indirect Illumination**: This is the light that has bounced off other objects before reaching the object. This accounts for soft shadows, reflections, and color bleeding.

Global illumination models take both direct and indirect illumination into account, creating more realistic lighting by simulating how light behaves in a real environment.

## Global Illumination Equation

In simplified terms, the total light reflected from a surface can be written as:

- **Equation**:  
  `'L_total = L_direct + L_indirect'`

Where:

- `L_total`: The total amount of light reflected from the surface.
- `L_direct`: The light directly from a light source.
- `L_indirect`: The light that has bounced from other objects (also called **bounce light**).

This creates more **natural-looking** scenes because it takes into account how light interacts with the entire environment.

## Example of Global Illumination

Imagine a room lit by a window. The sunlight not only directly illuminates the floor but also **bounces** off the walls and ceiling, softly lighting the entire room. This effect is due to **global illumination**.

### Real-World Applications

Global illumination is used in rendering and computer graphics to create realistic lighting effects such as:

- **Soft shadows**: Light that bounces around creates softer shadows instead of harsh, sharp ones.
- **Color bleeding**: Light bouncing from a colored surface (e.g., a red wall) can make nearby surfaces appear slightly red.
- **Ambient occlusion**: Small crevices and tight spaces appear darker because less light can reach them.

## Simplified Definition

- **Global Illumination**: A method of lighting that simulates how light interacts with all surfaces in a scene, including light bouncing and soft shadows.

### Visualizing Global Illumination

Think of a **well-lit room** with white walls. Even though the light source is a window, the entire room is softly lit because light is bouncing off the walls, ceiling, and floor. This is an example of **global illumination**.

## Differences Between Direct and Global Illumination

- **Direct illumination** only considers light coming directly from a source.
- **Global illumination** includes light bouncing off other objects, making it more realistic.

## References

Adapted from Szeliski, Richard. *Computer Vision: Algorithms and Applications (Texts in Computer Science)*. Springer International Publishing.
