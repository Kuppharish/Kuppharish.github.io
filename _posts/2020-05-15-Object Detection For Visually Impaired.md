---
layout: post
title: Object Detection For Visually Impaired
driveId: 1NKET_mgxJQzQl-uxJY3vNuYe5fQo_wvx
---

# Introduction: #
The goal of this project to build a system where object detection can be performed from the smartphone camera and the person can hear the details of the object pointed by the finger i.e, its name and distance from themself.

# Methodology: #
The whole project is divided into three major parts:
Transfering the image feed from phone camera to RasPi through WiFi which has been done with the help of an app called IP Web Cam.
Wrist Detection in order to detect the finger pointer from the image.
Object Detection of the surrounding objects to recognize the objects.

## Wrist and Object Detection ##
This is the key aspect of the whole project. Since RasPi has a very low computation capability, I chose YoloV3-tiny for object detection. 
Instead of using two different models for both the tasks I trained a modified Yolo model by changing the output layer to accomodate one additional class to dectect the wrist as an object.
Once the wrist is detected the finger tip is detected with the use of contour detection.

# Result: #
Final output video:
{% include googleDrivePlayer.html id=page.driveId %}
