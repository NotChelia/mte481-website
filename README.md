# mte481-website
Temporary Website to track work being done on MTE481 Project

# Group
David Qiu, Jason Xue, Diego Johnson, Aryan Gosalia, Mogbekeloluwa Adesiyun

# Current Status (Summary)

Finished final design, comprised of bogie-rocker frame, FLIR Sensor, 3D lidar with Point-LIO, (Diego can you add something about the electrical deisgn here)

# Subsystem Investigations

### Mapping Investigation Progress - David Qiu

#### Week 1
Drafting Requirements with team

#### Week 2
- Very easily singled out a 3D lidar as the best option, other options include 2d lidar, visual slam, but they all don't work for our use case where we cant assume lighting conditions
- Making progress on what potential algorithms could be used

#### Week 4
- Narrowed it down to Point-LIO, found a LIDAR that supported this, found the Unitree 4D LiDAR L1
- Bought the lidar for testing on amazon, will return if this doesnt work within 1 month

#### Week 5
- Summarizing current findings for PDP

#### Week 8
- Lidar found to have some poor software support, only includes source code for Ros Noetic which would be extremely limiting for our use case
- Work refactoring existing code for Ros 2 Humble start

#### Week 9
- Some success, still additional work needs to be made to prove that mapping works
<img src="https://i.imgur.com/mc4TnfY.png" width="80%" alt="Bad_MAP">

#### Week 11 
- Proved through simulation that this works
- Used two objects, cylinder and rectangle, with a 10x15x20 cm box and 50cm height and 10 cm radius cylinder as potential obstacles
<img src="https://i.imgur.com/11e95fB.png" width="80%" alt="Rviz_demo">
- Resulting Final Map
<img src="https://i.imgur.com/e7VGJ7Y.png" width="80%" alt="Final PCL">

### Conclusions
- Mapping about finalized, current solution proves to work, some additional work required to refactor to Ros2 Humble but overall Mapping is finalized and now efforts should be focused on integrating the scans to be used in Planning

### Firmware Progress -  Mogbekeloluwa Adesiyun

#### Week 1
- Evaluation of effectiveness of STM32 microcontroller vs ESP32 microcontroller
- Research Wifi capabilities of STM32 vs ESP32

#### Week 2
- Research on how to use PWM with motor encoders for ESP32
- Research on how to get speed data from motor encoders

#### Week 4
- Review of datasheets for ICs for microcontroller

#### Week 5
- Summarizing current findings for PDP

#### Week 8
- Continuation of review of datasheets for ICs 

#### Week 9
- Currently working on firmware that interacts with electrical components and microcontroller

#### Week 11 
- More work on firmware that interacts with electrical components and microcontroller

### Conclusions
- Selected ESP32 as microcontroller for project.  Researched the most efficient way to use PWM in ESP32 and STM32 microcontrollers. Currently working on designing and implementing firmware to communicate with ICs and sensors using ESP32 microcontroller
