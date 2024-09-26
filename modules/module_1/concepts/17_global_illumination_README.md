# Global Illumination (Ray Tracing and Radiosity)

### What is Global Illumination?
- **Definition**: Global Illumination (GI) refers to a group of algorithms in computer graphics that aim to simulate the way light interacts with surfaces in a scene, accounting for both direct and indirect light. Unlike local illumination models, which only consider direct light from light sources, global illumination captures the full complexity of light behavior in a scene, including reflections, refractions, and color bleeding.

### Key Techniques in Global Illumination:
1. **Ray Tracing**:
   - **Definition**: Ray tracing is a rendering technique that simulates the way rays of light travel in a scene. It traces the paths of rays from the eye (camera) into the scene, calculating color and brightness based on intersections with objects, light sources, and material properties.
   - **Key Features**:
     - **Reflections**: Calculates mirror-like reflections by recursively tracing rays from reflective surfaces.
     - **Refractions**: Models the bending of light as it passes through transparent materials.
     - **Shadows**: Determines shadowed regions by tracing rays to light sources to see if they are blocked.
   - **Advantages**:
     - Produces highly realistic images with accurate light interactions.
   - **Disadvantages**:
     - Computationally expensive and can be slow for complex scenes, especially with high levels of reflection and refraction.

2. **Radiosity**:
   - **Definition**: Radiosity is a rendering technique focused on the diffuse transfer of light in a scene. It calculates the light energy exchange between surfaces based on their emission, reflectance, and the geometry of the scene.
   - **Key Features**:
     - Models how light bounces off surfaces, leading to soft shadows and color bleeding effects.
     - The scene is typically divided into small patches, and energy exchange is calculated between these patches.
   - **Advantages**:
     - Provides a more accurate representation of light distribution, especially in scenes with complex interreflections.
   - **Disadvantages**:
     - Less effective for simulating specular reflections and can be less intuitive in handling dynamic light sources.

### Comparing Ray Tracing and Radiosity:
- **Ray Tracing**:
  - Best for scenes with complex reflections, refractions, and specular highlights.
  - Computes light paths directly from the camera's perspective.

- **Radiosity**:
  - Best for scenes with primarily diffuse surfaces, where light bounces and diffuses between surfaces is critical.
  - Computes light energy distribution across surfaces.

### Applications of Global Illumination:
1. **Film and Animation**:
   - Used in producing high-quality visual effects and realistic animations by accurately simulating light interactions.

2. **Architectural Visualization**:
   - Helps in rendering realistic lighting scenarios for buildings and interiors, allowing architects to visualize how natural and artificial light will affect spaces.

3. **Video Games**:
   - Techniques like ray tracing are increasingly used in real-time rendering to create realistic lighting and shadows in modern games.

### Summary:
- **Global Illumination** encompasses techniques like **Ray Tracing** and **Radiosity** to simulate realistic lighting in 3D environments.
- Ray tracing excels at handling complex light behaviors, while radiosity focuses on diffuse interreflection. Both techniques enhance the realism of computer-generated imagery but come with their own computational costs and strengths.