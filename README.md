# CamScanner using Python & OpenCV

Building a document scanner with OpenCV can be accomplished in just three simple steps:

- Step 1: Detect edges.
- Step 2: Use the edges in the image to find the contour (outline) representing the piece of paper being scanned.
- Step 3: Apply a perspective transform to obtain the top-down view of the document.


## Problem Facing

Canny Edge detection & Extraction of biggest contour:

After image blurring & thresholding, the next step is to find the biggest contour (biggest bounding box) and crop out the image. This is done by using Canny Edge Detection followed by extraction of biggest contour using four-point transformation.

The edges, pass the image through `cv2.findcontours()`. It joins all the continuous points (along the edges), having same colour or intensity. After this we will get all contours — rectangles, spheres, etc

Use `cv2.convexHull()` and `cv2.approxPolyDP` to find the biggest rectangular contour(approx) in the photo.
