# Self-Driving Car Engineer Nanodegree

## Project: **Advanced Lane Finding on the Road**

The goals / steps of this project are the following:

* Compute the camera calibration matrix and distortion coefficients given a set of chessboard images.
* Apply a distortion correction to raw images.
* Use color transforms, gradients, etc., to create a thresholded binary image.
* Apply a perspective transform to rectify binary image ("birds-eye view").
* Detect lane pixels and fit to find the lane boundary.
* Determine the curvature of the lane and vehicle position with respect to center.
* Warp the detected lane boundaries back onto the original image.
* Output visual display of the lane boundaries and numerical estimation of lane curvature and vehicle position.


### Reflection

### 1. Pipeline Description.

My pipeline consisted of 6 steps, as follows:

* Camera Calibration and Distortion Correction - used to find out the parameters for reducing the distortion and then undistort the images using undistort function in opencv.

* Image Thresholding - used to generate a binary image where the lane lines are clearly visible from gradients on x and y directions, manginutude of the gradient, direction of the gradient, and color transformation.

* Perspective Transform and Images Warping - used to view a lane from above, this was useful for calculating the lane curvature.

* Lane Detection - used to extract the lane lines and color them.

* Curvature and Vehicle Position Identification - used to define the curvature of the road at a specific point and what is the vehicle offset from the center of the lane.

* Outputing Results.


### 2. Potential Pipeline Shortcomings


The current pipeline works very well to the situation it was design for. For example, it picks the yellow and white lanes, so it will not work well in situations were panes are blue, or pink, for example. Or when the curves are outside the chosen boundary region (and a too broad region will introduce noise).


### 3. Pipeline Possible Improvements 

Perhaps a combination of approachs can make the final result more robust. Or the algorithm can have different tunings for different roads, for example.
