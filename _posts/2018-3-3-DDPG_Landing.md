---
layout: post
title: Autonomous Landing of Drone on a moving platform using DDPG
---

# Introduction #
A novel method of Reinforcement Learning, Deep Deterministic Policy Gradient(DDPG) is used to tackle the problem of landing an autonomous drone on a moving platform with the use just simple data i.e, GPS coordinates and imu data of drone and the base. Many methods have been emloyed before to tackle these kind of problems making use of raw pixels which need a lot of computation power to train and also less accurate. In our work we have just used low level control variables which made the training both less computative and more accurate    

![_config.yml]({{ site.baseurl }}/images/gazebo_ss.jpg)
