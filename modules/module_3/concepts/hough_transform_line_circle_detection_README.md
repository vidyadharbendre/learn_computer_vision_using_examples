# Hough Transform for Line and Circle Detection

This project demonstrates the use of Hough Transform techniques to detect lines and circles in images. The process involves loading an image, preprocessing it, and then applying Hough Line and Circle Transforms to identify specific patterns in the image.

## Step-by-Step Plan

### Step 1: Introduce the Dataset

For this project, we use a simple image that contains:
- **Clear lines for Hough Line Transform** (e.g., road lanes or geometric patterns).
- **Circles for Hough Circle Transform** (e.g., coins or circular objects).

Ensure that the image has well-defined lines and circular shapes that can be detected using Hough Transform.

### Step 2: Preprocess the Image

Before applying Hough Transforms, we preprocess the image to ensure consistent input for both local and global detection. The preprocessing steps are as follows:

1. **Load the image in grayscale**: This simplifies the image by removing color information, which is unnecessary for edge and pattern detection.
2. **Apply Gaussian Blur**: The Gaussian blur helps reduce noise and smoothens the image, which makes edge detection more accurate.
3. **Apply Canny Edge Detection**: This step highlights the edges in the image, which is a critical input for Hough Transform methods to detect lines and circles.

### Steps to Run the Code

1. **Install Required Libraries**  
    You will need OpenCV to run the image processing techniques. Install it using the following:
    ```python
        pip install opencv-python
    ```
2. **Load the Image**
    Load the image using OpenCV's imread function. The image should be pre-saved in the correct folder, and it will be loaded as a grayscale image.
    ```python
    
    import cv2
    image = cv2.imread('image.jpg', cv2.IMREAD_GRAYSCALE)
    ```
3. **Apply Gaussian Blur**
    Use OpenCV's GaussianBlur to reduce noise:
    ```python
    blurred_image = cv2.GaussianBlur(image, (5, 5), 0)

    ```
4. **Canny Edge Detection**
    Detect edges in the image using the Canny edge detector:

    ```python
    edges = cv2.Canny(blurred_image, 50, 150)
    ```
5. **Apply Hough Line Transform**
    Detect straight lines in the image using the Hough Line Transform:

    ```python
    lines = cv2.HoughLinesP(edges, 1, cv2.cv2.PI/180, 100, minLineLength=50, maxLineGap=10)
    for line in lines:
    x1, y1, x2, y2 = line[0]
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2)

    ```

6. **Apply Hough Circle Transform**
    Detect circles in the image using the Hough Circle Transform:
    ```python
    circles = cv2.HoughCircles(edges, cv2.HOUGH_GRADIENT, 1, 20, param1=50, param2=30, minRadius=0, maxRadius=100)
    if circles is not None:
        circles = np.round(circles[0, :]).astype("int")
        for (x, y, r) in circles:
            cv2.circle(image, (x, y), r, (0, 255, 0), 4)
            cv2.rectangle(image, (x - 5, y - 5), (x + 5, y + 5), (0, 128, 255), -1)
    ```
    