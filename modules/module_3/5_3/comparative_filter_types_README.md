## Comparative Analysis of Filter Types

| **Filter Type**         | **Noise Reduction Effectiveness** | **Edge Preservation** | **Suitability for Salt-and-Pepper Noise** | **Effect on Fine Image Details** | **Typical Use Case**                  |
|-------------------------|-----------------------------------|-----------------------|-------------------------------------------|-----------------------------------|---------------------------------------|
| **Gaussian Filter**     | Moderate                         | Low                   | Moderate                                  | Blurs edges and details           | General noise reduction               |
| **Median Filter**       | High                             | High                  | Excellent                                 | Preserves edges                   | Effective for salt-and-pepper noise   |
| **Adaptive Gaussian Filter** | High                             | Very High             | Good                                      | Closely retains original details  | Advanced denoising with structure preservation |
| **Bilateral Filter**    | High                             | High                  | Moderate                                  | Preserves edges and details       | Retains textures, good for natural images |
| **Non-Local Means Filter** | Very High                        | Very High             | Moderate                                  | Retains most image details        | Detailed denoising for medical and satellite images |

### Description of Filters:

1. **Gaussian Filter**: Provides general smoothing but tends to blur edges, making it less ideal for images with fine details.
2. **Median Filter**: Strong at reducing salt-and-pepper noise by replacing each pixel with the median value within its neighborhood, preserving edges.
3. **Adaptive Gaussian Filter**: Dynamically adapts to image structure, achieving noise reduction and detail retention by varying strength across the image.
4. **Bilateral Filter**: Similar to Gaussian but preserves edges by applying a spatial and intensity-based weighting, often used for photos with natural textures.
5. **Non-Local Means Filter**: Compares patches of pixels to retain similar regions, offering high detail preservation and is often used in medical imaging.

This chart highlights each filter's key strengths and trade-offs to help guide filter selection based on specific image processing goals.
