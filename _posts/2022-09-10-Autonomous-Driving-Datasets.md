---
layout: post
title: Autonomous Driving Datasets
author: [Richard Kuo]
category: [Lecture]
tags: [jekyll, ai]
---

Autonomous Driving Datasets includes A2D2, ApolloScape, Argoverse, Berkeley DeepDrive, Cityscapes, Comma2k19, Google-Landmarks, KITTI Vision Benchmark Suite, ...

--- 
## Open-Source Autonomous Driving Datasets
1. [A2D2 Dataset for Autonomous Driving](https://www.a2d2.audi/a2d2/en.html)<br>
Released by Audi, the Audi Autonomous Driving Dataset (A2D2) was released to support startups and academic researchers working on autonomous driving. The dataset includes over 41,000 labeled with 38 features. Around 2.3 TB in total, A2D2 is split by annotation type (i.e. semantic segmentation, 3D bounding box). In addition to labelled data, A2D2 provides unlabelled sensor data (~390,000 frames) for sequences with several loops.

2. [ApolloScape Open Dataset for Autonomous Driving](http://apolloscape.auto/)<br>
Part of the Apollo project for autonomous driving, ApolloScape is an evolving research project that aims to foster innovation across all aspects of autonomous driving, from perception to navigation and control. Via their website, users can explore a variety of simulation tools and over 100K street view frames, 80k lidar point cloud and 1000km trajectories for urban traffic.
![](https://images.squarespace-cdn.com/content/v1/5e662d05298fd51947b065be/1623118246092-5GOSW6OQVM3KO1IDVZR6/apolloscape-lanemark-segmentation.gif?format=500w)

3. [Argoverse Dataset](https://www.argoverse.org/)<br>
Argoverse is made up of two datasets designed to support autonomous vehicle machine learning tasks such as 3D tracking and motion forecasting. Collected by a fleet of autonomous vehicles in Pittsburgh and Miami, the dataset includes 3D tracking annotations for 113 scenes and over 324,000 unique vehicle trajectories for motion forecasting. Unlike most other open source autonomous driving datasets, Argoverse is the only modern AV dataset that provides forward-facing stereo imagery.

4. [Berkeley DeepDrive Dataset](https://www.bdd100k.com/)<br>
Also known as BDD 100K, the DeepDrive dataset gives users access to 100,000 annotated videos and 10 tasks to evaluate image recognition algorithms for autonomous driving. The dataset represents more than 1000 hours of driving experience with more than 100 million frames, as well as information on geographic, environmental, and weather diversity.

5. [CityScapes Dataset](https://www.cityscapes-dataset.com/)<br>
CityScapes is a large-scale dataset focused on the semantic understanding of urban street scenes in 50 German cities. It features semantic, instance-wise, and dense pixel annotations for 30 classes grouped into 8 categories. The entire dataset  includes 5,000 annotated images with fine annotations, and an additional 20,000 annotated images with coarse annotations.
![](https://images.squarespace-cdn.com/content/v1/5e662d05298fd51947b065be/1623118354736-TECH4VM0QUF5S1MGYNPC/cityscapes-dataset.png?format=1500w)

6. [Comma2k19 Dataset](https://github.com/commaai/comma2k19)<br>
This dataset includes 33 hours of commute time recorded on highway 280 in California. Each 1-minute scene was captured on a 20km section of highway driving between San Jose and San Francisco. The data was collected using comma EONs, which features a road-facing camera, phone GPS, thermometers and a 9-axis IMU. 

7. [Google-Landmarks Dataset](https://ai.googleblog.com/2018/03/google-landmarks-new-dataset-and.html)<br>
Published by Google in 2018, the Landmarks dataset is divided into two sets of images to evaluate recognition and retrieval of human-made and natural landmarks. The original dataset contains over 2 million images depicting 30 thousand unique landmarks from across the world. In 2019, Google published Landmarks-v2, an even larger dataset with 5 million images and 200k landmarks.

8. [KITTI Vision Benchmark Suite](http://www.cvlibs.net/datasets/kitti-360/)<br>
First released in 2012 by Geiger et al, the KITTI dataset was released with the intent of advancing autonomous driving research with a novel set of real-world computer vision benchmarks. One of the first ever autonomous driving datasets, KITTI boasts over 4000 academic citations and counting.<br>
KITTI provides 2D, 3D, and bird’s eye view object detection datasets, 2D object and multi-object tracking and  segmentation datasets, road/lane evaluation detection datasets, both pixel and instance-level semantic datasets, as well as raw datasets.
![](https://images.squarespace-cdn.com/content/v1/5e662d05298fd51947b065be/1623118515861-LTHVVJHBA6RSJFXGJFMT/kitti-vision-benchmark-examples.png?format=1000w)

9. [LeddarTech PixSet Dataset](https://leddartech.com/solutions/leddar-pixset-dataset/)<br>
Launched in 2021, Leddar PixSet is a new, publicly available dataset for autonomous driving research and development that contains data from a full AV sensor suite (cameras, LiDARs, radar, IMU), and includes full-waveform data from the Leddar Pixell, a 3D solid-state flash LiDAR sensor. The dataset contains 29k frames in 97 sequences, with more than 1.3M 3D boxes annotated

10. [Level 5 Open Data](https://level-5.global/data/)<br>
Published by popular rideshare app Lyft, the Level5 dataset is another great source for autonomous driving data. It includes over 55,000 human-labeled 3D annotated frames, surface map, and an underlying HD spatial semantic map that is captured by 7 cameras and up to 3 LiDAR sensors that can be used to contextualize the data.

11. [nuScenes Dataset](https://www.nuscenes.org/)<br>
Developed by Motional, the nuScenes dataset is one of the largest open-source datasets for autonomous driving. Recorded in Boston and Singapore using a full sensor suite (32-beam LiDAR, 6 360° cameras and radars), the dataset contains over 1.44 million camera images capturing a diverse range of traffic situations, driving maneuvers, and unexpected behaviors.
![](https://images.squarespace-cdn.com/content/v1/5e662d05298fd51947b065be/1623118644069-5KCA7MBNLLO4W0SCHE0M/nuscenes-dataset-examples.jpeg?format=1500w)

12. [Oxford Radar RobotCar Dataset](https://robotcar-dataset.robots.ox.ac.uk/)<br>
The Oxford RobotCar Dataset contains over 100 recordings of a consistent route through Oxford, UK, captured over a period of over a year. The dataset captures many different environmental conditions, including weather, traffic and pedestrians, along with longer term changes such as construction and roadworks.
![](https://robotcar-dataset.robots.ox.ac.uk/images/pointcloud-broad-st.png)

13. [PandaSet](https://pandaset.org/)<br>
PandaSet was the first open-source AV dataset available for both academic and commercial use. It contains 48,000 camera images, 16,000 LiDAR sweeps, 28 annotation classes, and 37 semantic segmentation labels taken from a full sensor suite.

14. [Udacity Self Driving Car Dataset](https://public.roboflow.com/object-detection/self-driving-car)<br>
Online education platform Udacity has open sourced access to a variety of projects for autonomous driving, including neural networks trained to predict steering angles of the car, camera mounts, and dozens of hours of real driving data.
![](https://i.imgur.com/A5J3qSt.jpg)

15. [Waymo Open Dataset](https://waymo.com/open/#)<br>
The Waymo Open dataset is an open-source multimodal sensor dataset for autonomous driving. Extracted from Waymo self-driving vehicles, the data covers a wide variety of driving scenarios and environments. It contains 1000 types of different segments where each segment captures 20 seconds of continuous driving, corresponding to 200,000 frames at 10 Hz per sensor.

### KITTI 
<table>
  <tr>
  <td><img src="http://www.cvlibs.net/datasets/kitti/images/passat_sensors.jpg"></td>
  <td><iframe width="460" height="260" src="https://www.youtube.com/embed/KXpZ6B1YB_k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></td>
  </tr>
</table>

<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*

