# Writeup - Final Project: Track 3D-Objects Over Time

## Step 1. Single Target Tracking

### Use Extended Kalman Filter to Track Single Target with Lidar Measurement Over Time

This step involves the following tasks:
* Implement the predict() function for an EKF
* Implement the update() function for an EKF
* Use the EKF to track a single target with lidar measurement input over time and plot the RMSE for the single track

The RMSE plot for the single track is shown below:

![](/img/Step1_RMSE.png)

## Step 2. Track Management

### Initialize, Update and Delete Track

This step involves the following tasks:
* Initialize track state and estimation error covariance matrix based on lidar measurement
* Implement track management with the following subtasks:
     - Decrease track score if no associated measurement found
     - Delete tracks with low scores or big estimation error covariance
     - Increase score for tracks with associated measurements
     - Set track state to "tentative" or "confirmed" depending on the score
* Plot the RMSE for a single track

The RMSE plot for the single track is shown below:

![](/img/Step2_RMSE.png)

## Step 3. Data Association

### Use SNN to Associate Measurements to Tracks (Multi Target Tracking)

This step involves the following tasks:
* Use actual association matrix based on Mahalanobis distances for all tracks in the input track list and all measurements in the input meas_list
* Initialize the list of unassigned measurements and unassigned tracks with input track list and measurement list
* Loop through the following subtasks until the minumum association matrix entry in infinity (no more association found):
    - Implement calculation of the Mahalanobis distance between a track and a measurement, use gating function to reduce the association complexity by removing unlikely association pairs.
    - Find the minimum entry in the association matrix, delete corresponding row and column from the matrix
    - Remove corresponding track and measurement from list of unassigned tracks and measurements
    - Return the association pair found
* Plot the RMSE for multi tracks

The RMSE plot for multi tracks using lidar is shown below:

![](/img/Step3_RMSE.png)

## Step 4. Sensor Fusion

### Camera-Lidar Fusion

This step involves the following tasks:
* Implement a function to check whether an object lies in the sensor's field of view
* Implement nonlinear camera measurement function h
* Initialize camera measurement 
* Moke a movie to showcase tracking results
* Plot the RMSE for multi tracks

The RMSE plot for multi tracks using lidar and camera fusion is shown below:

![](/img/Step4_RMSE.png)

The tracking movie is included in result_movie folder: ![movie](/result_movie/my_tracking_results.zip)
Note the original avi file is larger than 25M (87M) so I had to put it to zip file.
 Which part of the project was most difficult for you to complete, and why?
Do you see any benefits in camera-lidar fusion compared to lidar-only tracking (in theory and in your concrete results)?
Which challenges will a sensor fusion system face in real-life scenarios? Did you see any of these challenges in the project?
Can you think of ways to improve your tracking results in the future?
