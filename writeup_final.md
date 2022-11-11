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

## Step 4. Sensor Fusion

### Camera-Lidar Fusion
Write a short recap of the four tracking steps and what you implemented there (EKF, track management, data association, camera-lidar sensor fusion). Which results did you achieve? Which part of the project was most difficult for you to complete, and why?
Do you see any benefits in camera-lidar fusion compared to lidar-only tracking (in theory and in your concrete results)?
Which challenges will a sensor fusion system face in real-life scenarios? Did you see any of these challenges in the project?
Can you think of ways to improve your tracking results in the future?
