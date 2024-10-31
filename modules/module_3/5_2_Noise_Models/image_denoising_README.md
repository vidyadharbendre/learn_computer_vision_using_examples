# Image Denoising with Gaussian and Median Filters

This project explores image denoising techniques, focusing on reducing salt-and-pepper noise while preserving essential image details. We compare Gaussian and Median filters, as well as an adaptive Gaussian approach, to balance noise reduction and edge preservation.

## Project Overview

This project demonstrates the application of:
- **Gaussian Filter** - A linear filter that applies uniform smoothing across the image, which may blur edges.
- **Median Filter** - A non-linear filter that is highly effective at reducing salt-and-pepper noise, preserving edges better than Gaussian filtering.
- **Adaptive Gaussian (Biased Gaussian) Filter** - An adaptive filter that dynamically adjusts its strength based on the surrounding pixel structure, aiming to preserve fine details while reducing noise.

## Explanation of Output

1. **Original Noisy Image**: Shows the original image with strong salt-and-pepper noise, characterized by prominent black and white dots.
2. **Gaussian Filtered**: Illustrates the effect of Gaussian filtering, where noise reduction is achieved at the cost of edge blurring.
3. **Median Filtered**: Demonstrates the effect of median filtering, effectively reducing noise while better preserving edges compared to the Gaussian approach.
4. **Adaptive Gaussian Filtered**: Shows the effect of an adaptive approach, where the filter strength varies based on the image structure, yielding significant noise reduction while preserving image details.

This approach provides a balance between reducing prominent noise and retaining the original signal, allowing for cleaner further processing.

## Details on Noise and Filtering

### Salt and Pepper Noise Characteristics
- Every pixel is affected by noise, especially in low-light conditions.
- When increasing filter size, noise is further reduced but often introduces background texture.
- Despite improvements, noise is often not fully removed.

### Filtering Techniques

#### Gaussian Filter (Linear)
- Applies a uniform filter across the entire image.
- Results in blurred edges and reduced overall image sharpness, especially for finer details.
- Higher filter values, such as 10 or higher, may excessively blur image details.

#### Median Filter (Non-Linear)
- Ideal for salt-and-pepper noise, effectively reducing it without heavily blurring edges.
- Preserves edges significantly better than Gaussian filtering.

#### Adaptive Gaussian Filter
- A combination of linear and non-linear techniques.
- For lighter regions, it achieves better results by removing noise effectively.
- When dynamically adjusted based on pixel context, this method closely retains the original image's texture and detail.
- Potentially, a filter could be designed to respond to the image's structure, allowing it to reduce noise effectively while preserving essential details.

## Comparative Analysis

| **Filter Type**         | **Noise Reduction** | **Edge Preservation** | **Suitability for Salt-and-Pepper Noise** | **Effect on Image Details** |
|-------------------------|---------------------|-----------------------|-------------------------------------------|------------------------------|
| Gaussian Filter         | Moderate            | Low                   | Moderate                                  | Blurs fine details           |
| Median Filter           | High                | High                  | Excellent                                 | Preserves edges              |
| Adaptive Gaussian Filter| High                | Very High             | Good                                      | Closest match to original    |

## Future Enhancements

- **Custom Bias Filters**: Experiment with filters that modify strength dynamically, adjusting based on image structure to retain clarity and detail.
- **Real-Time Adaptive Filtering**: Develop filtering techniques that analyze context, applying smoothing selectively to areas of high noise without affecting edges and fine structures.

## Conclusion

This project illustrates the effectiveness of combining linear and non-linear filtering methods to achieve optimal noise reduction and detail preservation. The Adaptive Gaussian approach, or biased filtering, is a promising direction for achieving noise reduction without compromising the image's essential details.




