# Camera-Callibration

The goal is to calibrate the camera from the checkerboards in the images, and estimate:

- Reprojection error across all images
- Reprojection error across bins
- Real World error across all images 
- Real World error across bins 
- Real World error of top view images


The ipython notebooks first extract images from the video given and then run the calibration procedure.
The input of each notebook is the directory in which the video lies.

The Reprojection error is calculated in `Checkerboard_Calibrator.ipynb`

To calculate the Real World error, a perspective transform is applied on the images, which warp the checkerboard corners to the 
actual corners.

The Real world error across images and bins is calculated in `Checkerboard_Calibrator_Real_World.ipynb`. 

The Real world error for top view 20 images is calculated in `Checkerboard_Calibrator_Real_World_Top_View.ipynb`. This is done because perspective
transform is an approximation of transferring a view to another and for top-view images it will be most accurate.
