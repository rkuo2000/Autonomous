---
layout: post
title: Autonomous Driving Algorithms
author: [Richard Kuo]
category: [Lecture]
tags: [jekyll, ai]
---

Autonomous Driving Alogirthms

---
## LiDAR-based 3D Object Detection Methods
<p align="center"><img src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/LiDAR_3D_Object_Detection_methods.png?raw=true"></p>

### YOLO3D
**Paper:** [YOLO3D: End-to-end real-time 3D Oriented Object Bounding Box Detection from LiDAR Point Cloud](https://arxiv.org/abs/1808.02350)<br>
**Code:** [maudzung/YOLO3D-YOLOv4-PyTorch](https://github.com/maudzung/YOLO3D-YOLOv4-PyTorch)<br>

![](https://github.com/maudzung/YOLO3D-YOLOv4-PyTorch/blob/master/docs/demo.gif?raw=true)
* **Inputs:** Bird-eye-view (BEV) maps that are encoded by **height, intensity and density** of 3D LiDAR point clouds.
* **The input size:** 608 x 608 x 3
* **Outputs:** 7 degrees of freedom (**7-DOF**) of objects: (`cx, cy, cz, l, w, h, θ`)

**YOLOv4 architecture**<br>
<img  width="70%" height="70%" src="https://github.com/maudzung/YOLO3D-YOLOv4-PyTorch/blob/master/docs/yolov4_architecture.png?raw=true">

---
### YOLO4D
**Paper:** [YOLO4D: A Spatio-temporal Approach for Real-time Multi-object Detection and Classification from LiDAR Point Clouds](https://openreview.net/pdf?id=B1xWZic29m)

![](https://d3i71xaburhd42.cloudfront.net/ad16b7bf2ee7c84823f69a3bee6a30aa07311073/4-Figure1-1.png)

---
## Camera-based 3D Object Detection Methods
<p align="center"><img src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/Camera_based_3D_Object_Detection_methods.png?raw=true"></p>

### Pseudo-LiDAR
**Paper:** [Pseudo-LiDAR from Visual Depth Estimation: Bridging the Gap in 3D Object Detection for Autonomous Driving](https://arxiv.org/abs/1812.07179)<br>
**Code:** [mileyan/pseudo_lidar](https://github.com/mileyan/pseudo_lidar)<br>

![](https://mileyan.github.io/pseudo_lidar/cvpr2018-pipeline.png)

<iframe width="555" height="312" src="https://www.youtube.com/embed/mNtXTTo6wzI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
---
### Stereo R-CNN based 3D Object Detection
**Paper:** [Stereo R-CNN based 3D Object Detection for Autonomous Driving](https://arxiv.org/abs/1902.09738)<br>
**Code:** [HKUST-Aerial-Robotics/Stereo-RCNN](https://github.com/HKUST-Aerial-Robotics/Stereo-RCNN)<br>

![](https://github.com/HKUST-Aerial-Robotics/Stereo-RCNN/blob/master/doc/system.png?raw=true)

---
## Monocular Camera-based Depth Estimation Methods
<p align="center"><img src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/Monocular_Camera_based_Depth_Estimation_methods.png?raw=true"></p>

### DF-Net
**Paper:** [DF-Net: Unsupervised Joint Learning of Depth and Flow using Cross-Task Consistency](https://arxiv.org/abs/1809.01649)<br>
**Code:** [vt-vl-lab/DF-Net](https://github.com/vt-vl-lab/DF-Net)<br>
* Model in the paper uses 2-frame as input, while this code uses 5-frame as input (you might use any odd numbers of frames as input, though you would need to tune the hyper-parameters)
* FlowNet in the paper is pre-trained on SYNTHIA, while this one is pre-trained on Cityscapes

![](https://d3i71xaburhd42.cloudfront.net/c01876292b5d1ce6e746fd2e2053453847905bb2/5-Figure3-1.png)

<iframe width="860" height="360" src="https://filebox.ece.vt.edu/~ylzou/eccv2018dfnet/short_teaser.mp4"></iframe>

---
## Depth Fusion Methods with LiDAR and Camera
<p align="center"><img src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/Depth_Fusion_methods_with_LiDAR_and_Camera.png?raw=true"></p>

### DFineNet
**Paper:** [DFineNet: Ego-Motion Estimation and Depth Refinement from Sparse, Noisy Depth Input with RGB Guidance](https://arxiv.org/abs/1903.06397)<br>
**Code:** [vt-vl-lab/DF-Net](https://github.com/vt-vl-lab/DF-Net)<br>

<img width="70%" height="70%" src="https://d3i71xaburhd42.cloudfront.net/8e1c2ef0816598866e110362583c1c4f570401d3/3-Figure2-1.png">
<img src="https://d3i71xaburhd42.cloudfront.net/8e1c2ef0816598866e110362583c1c4f570401d3/4-Figure3-1.png">
<img src="https://www.researchgate.net/profile/Ty-Nguyen-5/publication/331840392/figure/fig4/AS:737828568834049@1552923447261/Qualitative-results-of-our-method-left-RGB-guide-certainty-34-middle-ranking-1st.ppm">
![](https://github.com/vt-vl-lab/DF-Net/blob/master/misc/zou2018dfnet.gif?raw=true)

---
## 3D Object Detection Methods with LiDAR and Camera
<p align="center"><img src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/3D_Object_Detection_methods with LiDAR_and_Camera.png?raw=true"></p>

### PointFusion
**Paper:** [PointFusion: Deep Sensor Fusion for 3D Bounding Box Estimation](https://arxiv.org/abs/1711.10871)<br>
**Code:** [mialbro/PointFusion](https://github.com/mialbro/PointFusion)<br>

<img src="https://media.arxiv-vanity.com/render-output/5472384/x1.png">
<img width="70%" height="70%" src="https://media.arxiv-vanity.com/render-output/5472384/sun-qualitative-3x4.png">

---
### MVX-Net
**Paper:** [MVX-Net: Multimodal VoxelNet for 3D Object Detection](https://arxiv.org/abs/1904.01649)<br>
**Code:** [mmdetection3d/mvxnet](https://github.com/open-mmlab/mmdetection3d/tree/master/configs/mvxnet)<br>

![](https://d3i71xaburhd42.cloudfront.net/dafd2826ec24d0dbdf0f4df7b6f20e7e2448f802/2-Figure2-1.png)

---
### DeepVO
**Paper:** [DeepVO: Towards End-to-End Visual Odometry with Deep Recurrent Convolutional Neural Networks](https://arxiv.org/abs/1709.08429)<br>
**Code:** [ChiWeiHsiao/DeepVO-pytorch](https://github.com/ChiWeiHsiao/DeepVO-pytorch)<br>

![](https://www.researchgate.net/profile/Khaled-Alyousefi/publication/341427132/figure/fig4/AS:891775065534466@1589627152759/DeepVO-Deep-Learning-Architecture-8-In-the-proposed-network-RCNN-takes-a-sequence.jpg)
![](https://camo.githubusercontent.com/775dc6f938052fa29586fed4fde4a477280eda67514af884f7687fbea3e163d4/68747470733a2f2f696d6775722e636f6d2f766f307658676b2e706e67)
<iframe width="832" height="468" src="https://www.youtube.com/embed/M4v_-XyYKHY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---
## Pedestrain Behavior Prediction Methods
<p align="center"><img src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/Pedestrain_Behavior_Prediction_methods.png?raw=True"></p>

### Predicting Future Person Activities and Locations in Videos
**Paper:** [Peeking into the Future: Predicting Future Person Activities and Locations in Videos](https://arxiv.org/abs/1902.03748)<br>

![](https://github.com/rkuo2000/AI-course/blob/gh-pages/images/Peaking_Into_The_Future_overview.png?raw=true)

<table>
  <tr>
  <td><img src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/Peaking_Into_The_Future_PIM.png?raw=true"></td> 
  <td><img src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/Peaking_Into_The_Future_PBM.png?raw=true"></td>
  </tr>
</table>

### Spectral Trajectory and Behavior Prediction
**Papers:** [Forecasting Trajectory and Behavior of Road-Agents Using Spectral Clustering in Graph-LSTMs](https://arxiv.org/abs/1912.01118)<br>
**Code:** [Xiejc97/Spectral-Trajectory-and-Behavior-Prediction](https://github.com/Xiejc97/Spectral-Trajectory-and-Behavior-Prediction)<br>
<table>
<tr>
<td><img src="https://github.com/Xiejc97/Spectral-Trajectory-and-Behavior-Prediction/raw/master/figures/predict.png" width="260"></td>
<td><img src="https://github.com/Xiejc97/Spectral-Trajectory-and-Behavior-Prediction/raw/master/figures/results.gif" width="266"></td>
<td><img src="https://github.com/Xiejc97/Spectral-Trajectory-and-Behavior-Prediction/raw/master/figures/behavior.gif" width="260"></td>
</tr>
</table>


## Vehicle Behavior Prediction Methods
![](https://github.com/rkuo2000/AI-course/blob/gh-pages/images/Vehicle_Behvior_Modeling_and_Decision_Making.png?raw=true)

**[Autonomous Vehicle Papers](https://github.com/DeepTecher/AutonomousVehiclePaper)**

---
### End-to-End Deep Learning for Self-Driving Cars
**Blog:** [End-to-End Deep Learning for Self-Driving Cars](https://developer.nvidia.com/blog/deep-learning-self-driving-cars/)<br>

![](https://developer.nvidia.com/blog/parallelforall/wp-content/uploads/2016/08/data-collection-system-624x411.png)
![](https://developer.nvidia.com/blog/parallelforall/wp-content/uploads/2016/08/training-624x291.png)
<img width="512" height="512" src="https://developer.nvidia.com/blog/parallelforall/wp-content/uploads/2016/08/cnn-architecture-624x890.png">
<iframe width="740" height="416" src="https://www.youtube.com/embed/NJU9ULQUwng" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---
### End-to-End Learning of Driving Models
**Paper:** [End-to-End Learning of Driving Models with Surround-View Cameras and Route Planners](https://arxiv.org/abs/1803.10158)<br>

![](https://d3i71xaburhd42.cloudfront.net/951dede2758451825dceed238d356a3a984c3670/2-Figure1-1.png)

---
### End-to-end Learning in Simulated Urban Environments
**Paper:** [Autonomous Vehicle Control: End-to-end Learning in Simulated Urban Environments](https://arxiv.org/abs/1905.06712)<br>

![](https://media.springernature.com/original/springer-static/image/chp%3A10.1007%2F978-3-030-35664-4_4/MediaObjects/491680_1_En_4_Fig2_HTML.png)
![](https://d3i71xaburhd42.cloudfront.net/c567e98e6d7c9d6f74223315e729708553b38103/6-Figure1-1.png)

---
### NeuroTrajectory
**Paper:** [NeuroTrajectory: A Neuroevolutionary Approach to Local State Trajectory Learning for Autonomous Vehicles](https://arxiv.org/abs/1906.10971)<br>

![](https://www.researchgate.net/profile/Sorin-Grigorescu/publication/334155766/figure/fig2/AS:837409541455872@1576665401121/Local-state-trajectory-estimation-for-autonomous-driving-Given-the-current-position-of.ppm)
![](https://www.researchgate.net/profile/Sorin-Grigorescu/publication/334155766/figure/fig3/AS:837409541459968@1576665401194/Examples-of-synthetic-a-GridSim-and-b-real-world-occupancy-grids-The-top-images-in.ppm)
![](https://www.researchgate.net/profile/Sorin-Grigorescu/publication/334155766/figure/fig4/AS:837409541468160@1576665401291/Deep-neural-network-architecture-for-estimating-local-driving-trajectories-The-training.ppm)

---
### ChauffeurNet [(Waymo)](https://sites.google.com/view/waymo-learn-to-drive/)
**Paper:** [ChauffeurNet: Learning to Drive by Imitating the Best and Synthesizing the Worst](https://arxiv.org/abs/1812.03079)<br>
**Code:** [aidriver/ChauffeurNet](https://github.com/aidriver/ChauffeurNet)<br>

![](https://www.researchgate.net/profile/Mayank-Bansal-4/publication/329525538/figure/fig1/AS:702131904450561@1544412699075/Training-the-driving-model-a-The-core-ChauffeurNet-model-with-a-FeatureNet-and-an.png)

<table>
  <tr>
  <td><p>With Stop Signs Rendered</p><img src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/Waymo_WithStopSigns.gif?raw=true"></td>
  <td><p>No Stop Signs Rendered</p><img src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/Waymo_NoStopSigns.gif?raw=true"></td>
  </tr>
  <tr>
  <td><p>With Perception Boxes Rendered</p><img src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/Waymo_WithPerceptionBoxes.gif?raw=true"></td>
  <td><p>No Perception Boxes Rendered</p><img src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/Waymo_NoPerceptionBoxes.gif?raw=true"></td> 
  </tr>
</table>

**Github:** [Iftimie/ChauffeurNet](https://github.com/Iftimie/ChauffeurNet)<br>

![](https://github.com/Iftimie/ChauffeurNet/blob/master/assets/carla-sim.gif?raw=true)

<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*

