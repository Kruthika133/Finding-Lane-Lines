# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

My pipeline consisted of 6 steps 

- Converting all imaged to grayscale 
- Applying Gaussian smoothing
- Using Canny Edge Detection
- Selecting the region of interest
- Applying Hough Tranform line detection
- Combining images


In order to draw a single line on the left and right lanes, I modified the draw_lines() function by classifying and sorting the right and left lines according to slopes. Calculating the slopes and intercepts for linear fit using polyfit. Insert intercept and slope to find values of x.

Some of the shortcomings and possible improvements that can be made are :
The color conversion would work better with RGB--HSV--Grayscale conversion.
The points in the region of interest is arbitary and can have issues while in slope or due to interference of other vehicles etc.
The pipeline might fail in case of too many curves or other markings on the road
image processing speed can be improved and other ML methods can be used to detect the pipelines
Curve fitting can be better done by using regression sing maximum value of y as guidance for finding next points and can be further optimized for better pipelines



