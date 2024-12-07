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
