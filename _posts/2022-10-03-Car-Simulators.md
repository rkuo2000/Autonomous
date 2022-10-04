---
layout: post
title: Car Simulators
author: [Richard Kuo]
category: [Lecture]
tags: [jekyll, ai]
---

Car Simulators introduce CARLA, Microsoft AirSim.

---
## Car Simulators

### [CARLA](http://carla.org/)
**Paper:** [CARLA: An Open Urban Driving Simulator](http://proceedings.mlr.press/v78/dosovitskiy17a/dosovitskiy17a.pdf)<br>

<iframe width="730" height="411" src="https://www.youtube.com/embed/S2VIP0qumas" title="CARLA 0.9.13" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**[CARLA Simulator](https://github.com/carla-simulator/carla)**<br>
* [CARLA Documentation](https://carla.readthedocs.io/en/0.9.13/)
  - [ROS Bridge Documentation](https://carla.readthedocs.io/projects/ros-bridge/en/latest/)
* [CARLA Nightly Build (Linux)](https://carla-releases.s3.eu-west-3.amazonaws.com/Linux/Dev/CARLA_Latest.tar.gz)
* [CARLA Nightly Build (Windows)](https://carla-releases.s3.eu-west-3.amazonaws.com/Windows/Dev/CARLA_Latest.zip)

![](https://carla.readthedocs.io/en/0.9.13/img/carla_modules.png)
* **Traffic manager.** A built-in system that takes control of the vehicles besides the one used for learning. It acts as a conductor provided by CARLA to recreate urban-like environments with realistic behaviours.
* **Sensors.** Vehicles rely on them to dispense information of their surroundings. In CARLA they are a specific kind of actor attached the vehicle and the data they receive can be retrieved and stored to ease the process. Currently the project supports different types of these, from cameras to radars, lidar and many more.
* **Recorder.** This feature is used to reenact a simulation step by step for every actor in the world. It grants access to any moment in the timeline anywhere in the world, making for a great tracing tool.
* **ROS bridge** and Autoware implementation. As a matter of universalization, the CARLA project ties knots and works for the integration of the simulator within other learning environments.
* **Open assets.** CARLA facilitates different maps for urban settings with control over weather conditions and a blueprint library with a wide set of actors to be used. However, these elements can be customized and new can be generated following simple guidelines.
Scenario runner. In order to ease the learning process for vehicles,

---
### AirSim
**[Github](https://github.com/microsoft/AirSim)**<br> 
**[Document](https://microsoft.github.io/AirSim/)**<br>

Cars in AirSim
<iframe width="683" height="399" src="https://www.youtube.com/embed/gnz1X3UNM5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Drones in AirSim
<iframe width="709" height="399" src="https://www.youtube.com/embed/-WfTr1-OBGQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---
### Install AirSim
**[Releases](https://github.com/Microsoft/AirSim/releases)** (.zip)<br>

For **Windows**, the following environments are available:
1. AbandonedPark
2. Africa (uneven terrain and animated animals)
3. AirSimNH (small urban neighborhood block)
4. Blocks
5. Building_99
6. CityEnviron
7. Coastline
8. LandscapeMountains
9. MSBuild2018 (soccer field)
10. TrapCamera
11. ZhangJiajie

For **Linux**, the following environments are available:
1. AbandonedPark
2. Africa (uneven terrain and animated animals)
3. AirSimNH (small urban neighborhood block)
4. Blocks
5. Building_99
6. LandscapeMountains
7. MSBuild2018 (soccer field)
8. TrapCamera
9. ZhangJiajie

* **Download & Unzip** a environment (AirSimNH.zip)<br>
* Find the exe file, **click to run**<br>
> Windows : *AirSimNH/WindowsNoEditor/AirSimNH/Binaries/Win64/AirSimNH.exe* <br>
> Linux   : *AirSimNH/LinuxNoEditor/AirSimNH/Binaries/Linux/AirSimNH* <br>

<table>
  <tr>
  <td><iframe width="456" height="260" src="https://www.youtube.com/embed/G5ersvlGZMw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></td>
  <td><iframe width="456" height="260" src="https://www.youtube.com/embed/GtrQzdlFMFs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></td>
  </tr>
</table>

### User Interface
<img width="50%" height="50%" src="https://github.com/rkuo2000/AI-course/blob/gh-pages/images/AirSimNH_help.png?raw=true">
* press **F1** for hot-keys help
* press **Arrow-keys** or **A-S-W-D** to drive
* press **Backspace** to rest & restart
* press **Alt-F4** to quit AirSim
* press **0** for sub-windows (shown below)
* Press **REC** button for recording Car/Drone info

&emsp; recorded file path will be shown on screen

For Car, 
```
VehicleName TimeStamp   POS_X   POS_Y   POS_Z   Q_W Q_X Q_Y Q_Z Throttle    Steering    Brake   Gear    Handbrake   RPM Speed   ImageFile
```
![](https://github.com/rkuo2000/AI-course/blob/gh-pages/images/AirSimNH_rec_txt.png?raw=true)

For Drone,
```
VehicleName TimeStamp   POS_X   POS_Y   POS_Z   Q_W Q_X Q_Y Q_Z ImageFile
```

---
### Manual Drive 
[remote_control](https://microsoft.github.io/AirSim/remote_control/)
<table>
  <tr>
  <td><img src="https://microsoft.github.io/AirSim/images/AirSimDroneManual.gif"></td>
  <td><img src="https://microsoft.github.io/AirSim/images/AirSimCarManual.gif"></td> 
  </tr>
</table>

### [Reinforcement Learning in AirSim](https://microsoft.github.io/AirSim/reinforcement_learning/)
The simulation needs to be up and running before you execute dqn_car.py!!!

1. Keep AirSim Env running first<br>
`cd AirSimNH/LinuxNoEditor` <br>
`./AirSimNH.sh -ResX=640 -ResY=480 -windowed`<br>
(For Windows, click AirSimNH.exe to run, **Alt-Enter** will switch to windowed mode)

2. To train DQN model for 500,000 eposides [(RL with Car)](https://github.com/Microsoft/AirSim/tree/master/PythonClient/reinforcement_learning)<br>
&ensp;Open a Terminal on Linux / run Git-Bash on Windows<br>
`pip install gym`<br>
`pip install stable-baselines3`<br>
`cd ~`<br>
`git clone https://github.com/rkuo2000/AirSim` <br>
`cd ~/AirSim/PythonClient/reinforcement_learning` <br>
`python dqn_car.py` <br>

[dqn_car.py](https://github.com/rkuo2000/AirSim/blob/master/PythonClient/reinforcement_learning/dqn_car.py)<br>
![](https://github.com/rkuo2000/AI-course/blob/gh-pages/images/AirSimNH_DQN_Car.png?raw=true)

[a2c_car.py](https://github.com/rkuo2000/AirSim/blob/master/PythonClient/reinforcement_learning/a2c_car.py)<br>
![](https://github.com/rkuo2000/AI-course/blob/gh-pages/images/AirSimNH_A2C_Car.png?raw=true)

---
### [Autonomous Driving Cookbook](https://github.com/Microsoft/AutonomousDrivingCookbook)
<table>
  <tr>
  <td><img src="https://github.com/microsoft/AutonomousDrivingCookbook/raw/master/AirSimE2EDeepLearning/car_driving.gif?raw=true"></td>
  <td><img width="400" height="220" src="https://github.com/microsoft/AutonomousDrivingCookbook/raw/master/DistributedRL/car_driving_2.gif?raw=true"></td>
  </tr>
</table>

Currently, the following tutorials are available:

- [Autonomous Driving using End-to-End Deep Learning: an AirSim tutorial](https://github.com/microsoft/AutonomousDrivingCookbook/tree/master/AirSimE2EDeepLearning)
- [Distributed Deep Reinforcement Learning for Autonomous Driving](https://github.com/microsoft/AutonomousDrivingCookbook/tree/master/DistributedRL)

**[[AirSim settings]](https://microsoft.github.io/AirSim/settings/)**

---
### [Kaggle: AirSim End-to-End Learning](https://kaggle.com/rkuo2000/airsim-end-to-end-learning)
#### Build Model with input image and state (driving angle)
```
image_input_shape = sample_batch_train_data[0].shape[1:]
state_input_shape = sample_batch_train_data[1].shape[1:]

#Create the convolutional stacks
pic_input = layers.Input(shape=image_input_shape)

x = layers.Conv2D(16, (3, 3), activation='relu', padding='same')(pic_input)
x = layers.MaxPooling2D(pool_size=(2,2))(x)
x = layers.Conv2D(32, (3, 3), activation='relu', padding='same')(x)
x = layers.MaxPooling2D(pool_size=(2, 2))(x)
x = layers.Conv2D(32, (3, 3), activation='relu', padding='same')(x)
x = layers.MaxPooling2D(pool_size=(2, 2))(x)
x = layers.Flatten()(x)
x = layers.Dropout(0.2)(x)

#Inject the state input
state_input = layers.Input(shape=state_input_shape)
m = layers.concatenate([x, state_input])

# Add a few dense layers to finish the model
m = layers.Dense(64, activation='relu')(m)
m = layers.Dropout(0.2)(m)
m = layers.Dense(10, activation='relu')(m)
m = layers.Dropout(0.2)(m)
m = layers.Dense(1)(m)

model = models.Model(inputs=[pic_input, state_input], outputs=m)

model.summary()
```
#### Test Result
![](https://github.com/rkuo2000/AI-course/blob/gh-pages/images/AirSim_End_to_End_Learning.png?raw=true)

---
#### Azure
* [使用 Project Bonsai 自發系統進行機器教學](https://learn.microsoft.com/zh-tw/azure/architecture/solution-ideas/articles/autonomous-systems)

![](https://learn.microsoft.com/zh-tw/azure/architecture/solution-ideas/media/machine-teaching-1-2.png)

* [適用於 AGV 廠商無關通訊的 VDA 5050 規格實作](https://learn.microsoft.com/zh-tw/azure/architecture/example-scenario/iot/automated-guided-vehicles-fleet-control#implementation-of-the-vda-5050-specification-for-agv-vendor-agnostic-communication)

![](https://learn.microsoft.com/zh-tw/azure/architecture/example-scenario/iot/media/automated-guided-vehicles-fleet-control-03.png)


<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*

