# Image Processing Approaches

This repository demonstrates three fundamental approaches to image processing: 

1. **Per-Component Processing**
2. **Vector-Based Processing**
3. **Spatial Neighborhood Processing**

## 1. Per-Component Processing

In this approach, each color channel (Red, Green, and Blue) is treated as a separate grayscale image. Processing is applied independently to each channel, and the results are then combined to form the final RGB image.

### **Key Steps:**
- Load grayscale images for the R, G, and B components.
- Apply independent processing to each component (e.g., inverting, thresholding).
- Merge the processed components into a single RGB image.

### **Use Case:**
- Ideal when specific operations need to target individual color channels.

---

## 2. Vector-Based Processing

This approach treats the RGB image as a collection of color vectors. Processing is applied directly to the color pixels without separating the channels.

### **Key Steps:**
- Load the RGB image or combine grayscale components into an RGB image.
- Apply transformations or operations directly on the RGB image (e.g., brightness adjustment, color mapping).

### **Use Case:**
- Useful for operations that rely on relationships between color components or require simultaneous processing of all components.

---

## 3. Spatial Neighborhood Processing

This approach focuses on the spatial context of pixels, considering neighborhoods (local regions) around each pixel for processing. 

- **For Grayscale Images:** Process 2D neighborhoods (e.g., smoothing, edge detection).
- **For RGB Images:** Process 3D neighborhoods (color voxels) to preserve spatial and color coherence.

### **Key Steps:**
- Load a grayscale or RGB image.
- Apply filters such as Gaussian blur, sharpening, or edge detection.
- For RGB images, the processing extends to the color space (3D).

### **Use Case:**
- Essential for tasks like denoising, texture enhancement, and local pattern recognition.

---

## Summary of Approaches

| **Approach**               | **Processing Unit**    | **Examples**                                | **Use Cases**                                           |
|-----------------------------|------------------------|---------------------------------------------|--------------------------------------------------------|
| **Per-Component Processing** | Individual color channels (R, G, B) | Inverting, histogram equalization            | Color-based segmentation or individual channel analysis |
| **Vector-Based Processing**  | Color pixels (vectors) | Brightness adjustment, color mapping         | Global image transformations                           |
| **Spatial Neighborhood**     | Pixel neighborhoods (2D/3D) | Gaussian blur, sharpening, edge detection    | Image denoising, texture analysis, object detection    |

---

## How to Run the Programs

Each approach is implemented in a separate Python script. Clone this repository and follow these steps:

1. Place your grayscale or RGB images in the `data/images` folder.
2. Run the corresponding Python script for each approach:
   - `per_component_processing.py`
   - `vector_based_processing.py`
   - `spatial_neighborhood_processing.py`

3. View the results displayed using `matplotlib`.

---

## Dependencies

Ensure the following Python libraries are installed:
- `opencv-python`
- `numpy`
- `matplotlib`

Install them using pip:
```bash
pip install opencv-python numpy matplotlib
```