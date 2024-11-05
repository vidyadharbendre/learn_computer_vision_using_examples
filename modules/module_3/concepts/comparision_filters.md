## Image Processing Filters: Roberts, Prewitt, and Sobel

### Overview
In image processing, edge detection is a crucial step for identifying and highlighting important structures in an image. This section outlines three popular edge detection filters: **Roberts**, **Prewitt**, and **Sobel** filters.

### 5W1H Analysis

#### **Who**:
These filters are used by computer vision practitioners, graphic designers, and developers who work with image processing applications.

#### **What**:
- **Roberts Filter**: A simple, gradient-based edge detection filter that uses two 2x2 kernels to compute the gradient of the image intensity. It highlights edges by computing the difference between diagonally adjacent pixels.
  
- **Prewitt Filter**: Similar to Roberts, but uses two 3x3 kernels to calculate the gradient. It averages the differences in pixel intensities to enhance the edge features while reducing noise.
  
- **Sobel Filter**: An improvement over Prewitt, the Sobel filter also employs two 3x3 kernels. It emphasizes the vertical and horizontal edges while providing a more refined gradient magnitude calculation.

#### **When**:
These filters are typically used during the preprocessing stage of image analysis, especially when preparing images for further analysis, segmentation, or object detection.

#### **Where**:
- **Applications**: Image editing software, robotics, medical imaging, and autonomous vehicles, where edge detection is necessary for object recognition and scene understanding.

#### **Why**:
Edge detection is vital for:
- Identifying boundaries within images.
- Enhancing feature extraction.
- Reducing image noise, making subsequent analysis easier and more accurate.

#### **How**:
1. **Roberts Filter**:
   - Kernels:
     ```
     Gx = [[1, 0],
           [0, -1]]

     Gy = [[0, 1],
           [-1, 0]]
     ```
   - Apply the kernels to the image to compute the gradient.

2. **Prewitt Filter**:
   - Kernels:
     ```
     Gx = [[-1, 0, 1],
           [-1, 0, 1],
           [-1, 0, 1]]

     Gy = [[1, 1, 1],
           [0, 0, 0],
           [-1, -1, -1]]
     ```
   - Convolve the image with these kernels to obtain gradient magnitudes.

3. **Sobel Filter**:
   - Kernels:
     ```
     Gx = [[-1, 0, 1],
           [-2, 0, 2],
           [-1, 0, 1]]

     Gy = [[1, 2, 1],
           [0, 0, 0],
           [-1, -2, -1]]
     ```
   - Similar to Prewitt, but with a different emphasis on pixel values, leading to better edge detection performance.

### Conclusion
Roberts, Prewitt, and Sobel filters are foundational techniques in image processing for edge detection. Understanding their functionality and application helps in enhancing image analysis tasks in various domains.
