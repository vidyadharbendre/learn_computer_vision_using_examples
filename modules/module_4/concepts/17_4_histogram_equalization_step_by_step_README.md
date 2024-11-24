# Histogram Equalization - README

This document demonstrates the step-by-step process of calculating a histogram, cumulative distribution function (CDF), normalized CDF, and equalized pixel intensity values using a revised example.

---

## **Concept Overview**

### **1. Histogram**
- A histogram represents the frequency of pixel intensities in an image.
- Example:  
  Consider an image with **16 total pixels** and the following frequency distribution:

    Intensities: 0, 75, 175, 255 Frequencies: 4, 6, 4, 2

### **2. Cumulative Distribution Function (CDF)**
- The CDF represents the cumulative frequency of intensities.
- It is calculated by summing the frequencies progressively:

Intensities: 0, 75, 175, 255 CDF: 4, 10, 14, 16


### **3. Normalized CDF**
- The normalized CDF scales the CDF values to fit within the range of pixel intensities (0 to 255 for an 8-bit image).
- Formula:
`'Normalized CDF' = ('CDF_current' / 'Total Pixels') × 'Max Intensity (255)'`

#### Example:
For each intensity:
- `CDF = 4`: `Normalized CDF = (4 / 16) × 255 = 63.75` (rounded to `64`)
- `CDF = 10`: `Normalized CDF = (10 / 16) × 255 = 159.375` (rounded to `159`)
- `CDF = 14`: `Normalized CDF = (14 / 16) × 255 = 223.125` (rounded to `223`)
- `CDF = 16`: `Normalized CDF = (16 / 16) × 255 = 255`

### **4. Equalized Values**
- The normalized CDF directly provides the new intensity values for each original intensity:

Original Intensities: 0, 75, 175, 255 Equalized Intensities: 64, 159, 223, 255


---

## **Step-by-Step Calculation Example**

### **Input Data**
- Total pixels: `16`
- Frequency distribution:

Intensities: 0, 75, 175, 255 Frequencies: 4, 6, 4, 2


### **1. Compute Histogram**
- This is already provided as:

Frequencies: 4, 6, 4, 2


### **2. Compute CDF**
- Calculate the cumulative frequency:

Intensities: 0, 75, 175, 255 CDF: 4, 10, 14, 16


### **3. Normalize CDF**
- Use the formula `'Normalized CDF' = ('CDF_current' / 'Total Pixels') × 255`.

#### Calculations:
- For intensity `0`:

Normalized CDF = (4 / 16) × 255 = 63.75 → 64

- For intensity `255`:

Normalized CDF = (16 / 16) × 255 = 255 → 255


### **4. Equalized Intensities**
- Replace the original intensities with the corresponding normalized CDF values:

Original Intensities: 0, 75, 175, 255 Equalized Intensities: 64, 159, 223, 255


---

## **Summary**
- Histogram equalization redistributes intensity values over the full range (`0` to `255`) to enhance contrast.
- The CDF helps to map lower intensity values (e.g., `4` out of `16` pixels) to higher contrast levels (e.g., `64` out of `255`), making image details more visible.

---

## **Applications**
1. **Medical Imaging**: Enhances X-rays or MRI scans to reveal finer details.
2. **Satellite Imagery**: Improves contrast in low-light or hazy conditions.
3. **Computer Vision**: Improves object detection and feature extraction by increasing contrast.

---

### **Next Steps**
- Apply this concept to an actual image and visualize the histogram before and after equalization.
- Implement contrast stretching as an alternative technique for comparison.

---

