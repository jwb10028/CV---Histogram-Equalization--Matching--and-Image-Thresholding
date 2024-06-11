Here's a draft of a README for your GitHub repository:

---

# Computer Vision: Histogram Equalization, Matching, and Image Thresholding

## Overview

This repository contains the code and documentation for performing various computer vision techniques, including histogram equalization, histogram matching, and image thresholding. These techniques are fundamental for image processing tasks that enhance the visual quality of images, extract important features, and prepare images for further analysis.

## Table of Contents

1. [Introduction](#introduction)
2. [Histogram Equalization](#histogram-equalization)
3. [Histogram Matching](#histogram-matching)
4. [Image Thresholding](#image-thresholding)
5. [Usage](#usage)
6. [Results](#results)
7. [References](#references)

## Introduction

This project explores three key techniques in computer vision:

- **Histogram Equalization**: Enhances the contrast of images by redistributing pixel intensity values.
- **Histogram Matching**: Adjusts the pixel intensity distribution of an image to match that of another image.
- **Image Thresholding**: Segments an image into foreground and background based on pixel intensity values.

## Histogram Equalization

Histogram equalization is a method to improve the contrast of an image by using its histogram values. The process involves:

1. Calculating the histogram of the source image to get the distribution of pixel intensities.
2. Computing the cumulative distribution function (CDF) from the histogram.
3. Normalizing the CDF to fit the original intensity range (0-255 for 8-bit images).
4. Mapping each pixel value of the source image to a new value based on the normalized CDF, resulting in the equalized image.

### Example

Here are the `people.png` images before and after histogram equalization, along with their histograms and CDFs:

- **Before Equalization**
  - ![people.png](path_to_image)
  - Histogram: ![people_histogram.png](path_to_histogram)
  - CDF: ![people_cdf.png](path_to_cdf)
  
- **After Equalization**
  - ![people_equalized.png](path_to_image)
  - Histogram: ![people_equalized_histogram.png](path_to_histogram)
  - CDF: ![people_equalized_cdf.png](path_to_cdf)

## Histogram Matching

Histogram matching adjusts the pixel intensity distribution of a source image to match that of a target image. The process involves:

1. Calculating the probability density function (PDF) and CDF for both source and target images.
2. Mapping the source image's pixel values to new values based on the target image's CDF using a helper function that finds the closest matching value.
3. Creating the matched image using the mapped pixel values.

### Example

Here are some creative examples of histogram matching from an input target image to a source input image:

- **Source Original A**
  - ![source_original_a.png](path_to_image)
- **Target A**
  - ![target_a.png](path_to_image)
- **Matched A**
  - ![matched_a.png](path_to_image)

## Image Thresholding

Image thresholding segments an image into foreground and background based on pixel intensity values. This repository implements the Otsu thresholding method, which determines the optimal threshold value by maximizing the inter-class variance.

### Example

For image `b2_a`, the Otsu method chose a threshold value of 131. The resulting binary image is shown below:

- **Original Image**
  - ![b2_a.png](path_to_image)
- **Thresholded Image**
  - ![b2_a_otsu.png](path_to_image)

## Usage

To use the code in this repository:

1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/computer-vision-techniques.git
   cd computer-vision-techniques
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the scripts:
   - For histogram equalization: `python histogram_equalization.py`
   - For histogram matching: `python histogram_matching.py`
   - For image thresholding: `python image_thresholding.py`

## References

- Zeng, S., & Otsu, N. (n.d.). Transactions on systems, man, and Cybernetics. Xing zheng yuan guo ke hui ke zi zhong xin.

---
