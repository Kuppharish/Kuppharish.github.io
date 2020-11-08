---
layout: post
title: Optimized Implementation of LOAM for Indoor Environments.
---

# Introduction: #
LOAM is a state of the art algorithm developed for Lidar SLAM. Many major developments have taken place after the influx of LOAM and the next major developement was the [Lego_LOAM](https://github.com/RobustFieldAutonomyLab/LeGO-LOAM "Lego-LOAM") which was explicitly developed for Outdoor and Environments and AGVs. In our case we implements the SLAM on an AGV so this was preferred over original LOAM but we needed to make approriate adjustents for the sake of indoor environments.

# Hardware: #
A robot was built for testing iRobot Create2 as the base mobile robot and an Ouster OS1-64 was mounted on it. Nvidia Jetson TX2 was used for the onborad computing and lidar data was received over the WiFi.

![alt text][logo]

[logo]: https://github.com/Kuppharish/Kuppharish.github.io/blob/master/images/image.jpg


# Methodology: #
LegoLoam performs point cloud clutering and removes clusters with very small number of points deeming them not significant. While this is true for outdoor environments, in the indoor environments small objects should also be taken into consideration. For this purpose this thershold has been significantly reduced.

Since we are fixed on using the SLAM on AGVs, we can divide the registration into two parts where we match plane features and edge features seperately. This in itself reduces the complexity of the algorithm by about 30%. In this project, we used the multi cores of Jetson and made the above two regiatrations parallel with the help of concurrency in C++.  

# Result: #
The computation time of the LOAM algorithm has been reduced by 10% while keeping the accuracy same.
