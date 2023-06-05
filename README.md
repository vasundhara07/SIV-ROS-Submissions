# SIV-ROS Submissions
**Sensor Integration and Visualisation in ROS**

Submission repository for assignments of SIV-ROS project of Robotics Club 2023-24.



## Objective

- Introduce and familiarise mentees with ROS, Gazebo and Rviz
- Integrate the following in ROS:
  - Motor Encoders for Odometry data
  - LiDAR for SLAM (RPLiDAR A1M8 360 Degree)
  - IMU (MPU6050)
  - GPS (NEO-M8N GPS Module)
- **Simultaneously** take input from the sensors and visualise all the data in Rviz.
- Use teleop through ssh or use another kind of remote control along with gmapping node to use SLAM for creating the map of an environment in Rviz.

### Folder Structure

```bash

SIV-ROS-Submissions
├── Assignment-1
│   ├── 210353_DivyaGupta
│   │   ├── README.md
│   │   └── src
│   ├── 210369_EmaadAhmed
│   │   ├── README.md
│   │   └── src
│   └── 210684_OmShivamVerma
│       ├── README.md
│       └── src
├── LICENSE
└── README.md

```

#### How to Submit

Create a **fork** of this repository. This fork is where you will add all the solutions of your assignments. After creating your fork, and making some changes (your solutions), create a pull request with the title: ```Submission of <Name>, <Roll No.>```. This pull request should be created only once, 

Here ```src``` is the _source_ folder of your workspace. Also, create the ```README.md``` containing a brief description of what you have done.

## Assignment-1

**Aim:** Understanding nodes, topics, and their connection with sensors.

**Task:**
Create a package - “Image_processes” that can subscribe and publish topics from given nodes:
1. Node1 -: Publish webcam image frames to the topic “Webcam_img”. (“Webcam_img” topic takes image frames from webcam as data).
2. Node2 -: It will subscribe to the topic “Webcam_img” and publish data to the topic “Webcam_cropped”. (“Webcam_cropped” topic has image frames from webcam and crop  it by 30% in pixels).
3. Node3 -: It will subscribe to the topic “Webcam_cropped” and show it.

# Assignment 1: what I did
Created a package 'image_processes' containing 3 nodes
Node 1- captures image from the webcam and publishes it onto a topic
Node 2- subscribes from the topic, crops the captured image by 30% in pixels and publishes it onto another topic
Node 3- subscribes from topic and displays the image

**Edit:** Create a launch file named ```image_cropping.launch``` which launches all the nodes at once.
