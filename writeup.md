# **Finding Lane Lines on the Road** 


---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.


The pipeline consisted of the following steps:
1. [Pre-processing]: convert image into gray scale and blur it with Gaussian filter.
2. Use Canny edge detection to extract the contour.
3. Implement Region of Interests (ROI) and Hough transform to extract potential line.
4. [Post-processing]: colorize the detected lane and extropolate the dash-line into solid line.
5. [Post-processing]: use cv2.addWeighted function to overlap the mask and original image.



### 2. Identify potential shortcomings with your current pipeline


Shortcoming:
1. The assumption for "Hard" categorizing left and right line by the value of slope is not robust in curvature scenario
2. Hyper-parameters for Hough transform or Canny are that reliable if the driving scenario is changed.

### 3. Suggest possible improvements to your pipeline

Based on the description on section 2, the possible input will be using Convolutional Neural Network to detect the line first and use conventional method (what we have done) to fine tune the result. Since CNN is a more powerful image recognition approach and it can be relatively easlier to adapt to different driving scneario. 

However, additional work will be:
1. Model selection
2. Model training
3. Train/test sample collection
4. (optional) Data augmentation
5. Model performance profiling
