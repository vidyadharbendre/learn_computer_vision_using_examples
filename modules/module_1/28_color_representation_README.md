# Digital Imaging and Color Representation

## Overview

In digital imaging, each pixel in an image sensor has a specific color filter—either Red, Green, or Blue (RGB)—in front of it. A single pixel measures only one color at a time. However, neighboring pixels capture other colors, and since these pixels are arranged in a dense grid, the sensor collectively captures the entire color spectrum of the image.

The process of converting this raw color data into a full RGB image is known as **Demosaicing**. Since each pixel only records one color, interpolation is used to estimate the missing colors for each pixel, enabling the creation of the complete image.

## What is Demosaicing?

Demosaicing is a technique used to reconstruct a full color image from the incomplete color information captured by a digital sensor. The color filters in front of each pixel allow it to capture only one of the primary colors (Red, Green, or Blue). To achieve a full color image, the missing color values are calculated using data from neighboring pixels.

### Bayer's Pattern

A common arrangement of color filters used in image sensors is the **Bayer Pattern**, where 50% of the pixels are green, 25% are red, and 25% are blue. This is because the human eye is more sensitive to green light. Using interpolation, the missing color components are estimated for each pixel, resulting in a fully colored image.

## Formula: Color Ratios

To understand how color is represented in digital imaging, we can break down the contribution of each color channel using ratios. One of the most common methods is normalizing the color components.

For example, the red ratio is given by:

`r = R / (R + G + B)`

Similarly, the green and blue ratios can be represented as:

`g = G / (R + G + B)`

`b = B / (R + G + B)`

Here, `R`, `G`, and `B` represent the intensity values of red, green, and blue channels, respectively, for a pixel. This ratio helps represent how much of each color is contributing to the overall pixel color.

## Applications in HDR and Color Television

In **color television**, predefined ratios for red, green, and blue are used to match the display output with human perception. The calibration for each device ensures that the colors appear natural to the viewer.

In **HDR (High Dynamic Range)** imaging, different ratios are used to accommodate a wider range of brightness and contrast. HDR cameras and screens can capture and display a broader range of light intensities, resulting in richer, more vibrant images.

---

This README serves as an introduction to digital image processing, explaining how optical images are converted into digital data, the basics of demosaicing, and how color ratios help in representing images across different media formats.
