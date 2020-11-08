---
layout: post
title: Optimized Implementation of LOAM for Indoor Environments.
---

# Introduction: #
LOAM is a state of the art algorithm developed for Lidar SLAM. Many major developments have taken place after the influx of LOAM and the next major developement was the [Lego_LOAM](https://github.com/RobustFieldAutonomyLab/LeGO-LOAM "Lego-LOAM") which was explicitly developed for Outdoor and Environments and AGVs. In our case we implements the SLAM on an AGV so this was preferred over original LOAM but we needed to make approriate adjustents for the sake of indoor environments.

# Hardware: #
A robot was built for testing iRobot Create2 as the base mobile robot and an Ouster OS1-64 was mounted on it. Nvidia Jetson TX2 was used for the onborad computing and lidar data was received over the WiFi.
![alt text](https://github.com/Kuppharish/Kuppharish.github.io/blob/master/images/image.png)


# Methodology: #
First a huge number of images of cows and other Livestock were obtained by the drone.  
Using these images training waas done using the state-of-the-are Faster RCNN technique.    
A new indegenous algorithm is developed to count the number of cows from a continious video.

# Result: #
Final output video:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=M2gHWYT-obE" target="_blank">
 <img src="https://github.com/Kuppharish/Kuppharish.github.io/blob/master/images/count_tn.jpg?raw=true" alt="Livestock Monitoring" width="600" height="350" border="10" />
</a>

#### Disclaimer : Due to confidentiality issues much information couldn't be presented. ####
