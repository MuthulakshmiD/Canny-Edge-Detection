# Canny-Edge-Detection
### Project Title

## Canny Edge Detection

### Overview

This project implements the Canny edge detection method.
Canny is a multi-stage algorithm that finds edges in images.
It aims to detect true edges while reducing noise and false detections.

### Key Features

• Smooths image to reduce noise.

• Detects intensity gradients.

• Suppresses non-maximum pixels to thin edges.

• Applies double-thresholding and edge tracking by hysteresis.

• Produces clean, thin edge maps suitable for further processing.

### When to Use

Use Canny when you need:

• Clean edge maps for object detection or shape analysis.

• Good balance between detection sensitivity and noise rejection.

• Preprocessing for computer vision tasks (e.g., segmentation, feature extraction).

## Algorithm — High-level Steps

• Noise reduction — Smooth the image with a Gaussian filter.

• Gradient computation — Compute gradient magnitude and direction (edge strength and orientation).

• Non-maximum suppression — Thin edges by keeping only local maxima in gradient direction.

• Double thresholding — Classify pixels as strong, weak, or non-relevant using two thresholds.

• Edge tracking by hysteresis — Keep weak pixels that are connected to strong ones; discard the rest.

## Input

• A grayscale image (single channel) or a color image converted to grayscale.

• Optional: parameters such as Gaussian kernel size, low threshold, high threshold, and sigma for smoothing.

## Output

• A binary edge image (pixels either edge or non-edge).

• Optionally, visual overlay of detected edges on original image.

## Expected Results

• Thin, connected edge lines that follow object boundaries.

• Reduced spurious edges in smooth regions.

• Robust detection under moderate noise if parameters are tuned.

## Common Applications

• Object boundary detection.

• Feature extraction for recognition tasks.

• Preprocessing for segmentation.

• Medical image analysis and industrial inspection.

## License

Use and adapt this README freely. Include proper attribution if you reuse substantial parts in published work.

John Canny, “A Computational Approach to Edge Detection”, IEEE Transactions on Pattern Analysis and Machine Intelligence, 1986.

Standard computer vision textbooks and OpenCV documentation on Canny.
