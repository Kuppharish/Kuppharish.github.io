---
layout: post
title: State Esitmation using VIO
---

# Introduction: #
Here we are working on a Micro Air Vechicle, which has a camera and an IMU sensor mounted on it and the MAV is driven . The whole project is composed of three different parts where in the first part we estimate the pose of MAV using a mat of April Tags present on the ground. In the later part we estimate the linear and angular velocity of the MAV using Optical Flow. In the final part we use Extended Kalman Filter where IMU data is considered for prediction and measurement is done using the results of vision.

The state and its differential considered for EKF are,

![EKF-1](/images/EKF-1.PNG)
![EKF-2](/images/EKF-2.PNG)

