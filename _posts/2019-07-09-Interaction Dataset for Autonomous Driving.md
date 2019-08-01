---
title: Interaction Dataset for Autonomous Driving
layout: post
categories: ''
tags: U.C.Berkeley
img: track.jpg
---
Nowadays, for automation driving, perception, planning and decision is of high significance. Our project is aimed at building an interaction dataset from bird's eye view, to demonstrate naturalistic motions of various traffic participants in a variety of highly interactive driving scenarios.

##General Introduction
In our project, I have taken three parts of the work.1.Object detection for both vehicles and pedestrians.2.Object tracking for pedestrian. 3.Self-merging algorithm and manual verification GUI for verification.

Our project's website is [here](http://interaction-dataset.com/).

![Our Procedure]({{site.baseurl}}/assets/img/procedure.png)

##Detection
As for detection, I retrained Mask RCNN and add fore-ground mask as the 4th channel, and the average precision achieves __90.3% __for vehicle and __87.6%__ for pedestrian. The basic framework can be found [here](https://github.com/matterport/Mask_RCNN)
>>>>>>> dbd180e6ff24a299f734b547b4be847bd99d3ca5

![Framework]({{site.baseurl}}/assets/img/framework.jpg)

![Detection]({{site.baseurl}}/assets/img/detect.jpg)

##Tracking and Verification
For object tracking, I applied __Kernelized Correlation Filters__(KCF) algorithm and achieve good results for pedestrian. For verification, I used KLT algorithm to find some broken track pairs and apply __Kalman Filter__ to estimate their states and merge them into one track. Besides, I have developed a GUI for manual verification.

![Auto_verification]({{site.baseurl}}/assets/img/merge.jpg)