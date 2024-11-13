# Hough Transform

The Hough Transform is a powerful image processing technique used for detecting geometric shapes (such as lines, circles, or ellipses) in an image. It works by transforming a point in the image space into a curve in a parameter space, making it easier to detect shapes.

---

## How It Works

### Representation in Parameter Space

#### For Lines:
A line in the Cartesian coordinate system `'y = mx + c'` can be represented in the Hough Transform space as:

`r = x * cos(θ) + y * sin(θ)`

Where:
- **`r`:** The perpendicular distance from the origin to the line.
- **`θ`:** The angle the line makes with the x-axis.

#### For Circles:
A circle can be represented by its center `'(a, b)'` and radius `'r'`.

---

### Accumulator Matrix

The Hough Transform uses an **accumulator matrix** to vote for potential shapes:
- Each point in the **image space** contributes votes to possible shapes in the **parameter space**.

---

### Finding Shapes

- **Peaks in the accumulator matrix** correspond to the most likely shapes (e.g., lines or circles) in the image.

---

## Applications

1. **Line Detection:** E.g., detecting lanes in autonomous driving.
2. **Circle Detection:** E.g., detecting circular objects like coins.
3. **General Shape Detection:** Useful in noisy images.

---

## Local vs Global Detection

### Local Detection
- **Definition:** Detects shapes within a specific region of the image.
- **Use Case:** Useful when the region of interest (ROI) is small or predefined.
- **Examples:** Detecting circles in a specific part of an image.

### Global Detection
- **Definition:** Detects shapes across the entire image.
- **Use Case:** Useful when the shapes can appear anywhere in the image.
- **Examples:** Detecting lines in an entire image for road boundaries.

---

## Key Differences Between Local and Global Detection

| Aspect        | Local Detection                | Global Detection              |
|---------------|--------------------------------|--------------------------------|
| **Scope**     | Limited to a specific region  | Covers the entire image       |
| **Performance** | Faster and less resource-intensive | Slower and computationally expensive |
| **Use Case**  | Small regions, localized features | Large-scale or global analysis |

