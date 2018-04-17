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

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]

The pipeline consisted of the following steps:
1. [Pre-processing]: convert image into gray scale and blur it with Gaussian filter.
2. Use Canny edge detection to extract the contour.
3. Implement Region of Interests (ROI) and Hough transform to extract potential line.
4. [Post-processing]: colorize the detected lane and extropolate the dash-line into solid line.
5. [Post-processing]: use cv2.addWeighted function to overlap the mask and original image.



### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
