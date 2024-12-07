# mte481-website
Temporary Website to track work being done on MTE481 Project

# Group
David Qiu, Jason Xue, Diego Johnson, Aryan Gosalia, Mogbekeloluwa Adesiyun

# Current Status (Summary)

Finished final design, comprised of bogie-rocker frame, FLIR Sensor, 3D lidar with Point-LIO, Custom PCB with power distribution and motor control

## Weekly Log

#### Week 1 (Sept 9th)
Finalized roles in team and distributed tasks to each member
* David and Jason: Software
* Mogbekeloluwa and Diego: Electrical and Firmware
* Aryan: Mechanical

#### Week 2 (Sept 16th)
Group: Settled on the problem of search and rescue in partially damaged strucures
* David:
  * Researched localization and mapping techniques inluding 3D lidar as the best option, other options include 2d lidar, visual slam
* Jason:
  * Researched methods to detect survivors
  * Research mesh radio systems to allow communication back to offboard compute server
* Mogbekeloluwa:
  * Evaluation of effectiveness of STM32 microcontroller vs ESP32 microcontroller
  * Research Wifi capabilities of STM32 vs ESP32
* Diego:
  * Looked into motor specs and power requirements for various drone types
* Aryan:
  * 

#### Week 3 (Sept 23rd)
Group: Narrowed down problem into need, problem statement and constraints and criteria
* David:
  * Defined need and problem statement
* Jason:
  * Found some hardware like FLIR Leptons which were relatively cheap and can provide thermal imaging well enough to detect people
* Mogbekeloluwa:
  * Research on how to use PWM with motor encoders for ESP32
  * Research on how to get speed data from motor encoders
* Diego:
  * Determined final constraints and criteria and defined metrics for them
* Aryan:
  * 

#### Week 4 (Sept 30th)
Group: Found required patents and alternative solutions
* David:
  * Narrowed it down to Point-LIO, found a LIDAR that supported this, found the Unitree 4D LiDAR L1
  * Bought the lidar for testing on amazon, will return if this doesnt work within 1 month
* Jason:
  * Found some other alternatives such as experiemental microphone array from chinese research paper
* Mogbekeloluwa:
  * Review of datasheets for ICs for microcontroller
* Diego:
  * Started looking into possible chips to use for motor control and voltage regulation
* Aryan:
  * 

#### Week 5 (Oct 7th)
Group: Used descision matricies to select the best solution based on our criteria and constraints
* David:
  * Lidar found to have some poor software support, only includes source code for Ros Noetic which would be extremely limiting for our use case
  * Work refactoring existing code for Ros 2 Humble start
* Jason:
  * Pivoted to using onboard computer for Mapping, removing requirement for offboard computer server
  * No longer any radio work from this point onwards
* Mogbekeloluwa:
  * Decided on PID control for motors using feedback from motor encoders
* Diego:
  * Decided on specs for planetary gearmotors with built in encoders to go with the selected bogie rocker design
* Aryan:
  * 

#### Weeks 6 and 7 (Oct 21st)
Group: Prepared for PDP
* David:
  * Navigation slides for PDP
* Jason:
  * Created PDP slides for POI Identification
* Mogbekeloluwa:
  * Constraints and Criteria slides for PDP
* Diego:
  * Worked on intro for PDP
* Aryan:
  * Created drive system slides for PDP

#### Weeks 8 and 9 (Nov 4th)
Group: Started working on detailed design
* David:
  * Some success with mapping, still additional work needs to be made to prove that it works
    <img src="https://i.imgur.com/mc4TnfY.png" width="80%" alt="Bad_MAP">
* Jason:
  * Looked into how to SLAM navigation algorithms
* Mogbekeloluwa:
  * Continuation of review of datasheets for ICs 
* Diego:
  * Created electrical system overview flowchart
  * Solidified each electrical subsytem and their requirements
* Aryan:
  * 

#### Week 10 (Nov 11th)
Group: Began verifying various subsytem design 
* David:
  * Proved through simulation that this works
  * Used two objects, cylinder and rectangle, with a 10x15x20 cm box and 50cm height and 10 cm radius cylinder as potential obstacles
  <img src="https://i.imgur.com/11e95fB.png" width="80%" alt="Rviz_demo">
  * Resulting Final Map
  <img src="https://i.imgur.com/e7VGJ7Y.png" width="80%" alt="Final PCL">
* Jason:
  * Decided on using 3D occupancy grid with A* based on inspiration from MTE544
* Mogbekeloluwa:
  * Currently working on firmware that interacts with electrical components and microcontroller
* Diego:
  * Created schematic for electrical design
  * Made most final decisions for electrical component selection
* Aryan:
  * 

#### Weeks 11 and 12 (Nov 25th)
Group: Completed most of the detailed design and FDP
* David:
  * Worked on mapping slides for FDP
* Jason:
  * Decided on OctoMap implementation for occupancy grid, custom 2D costmap calculation, A* and Trajectory Rollout method for navigation
  * Wrote slides for FDP on navigation
* Mogbekeloluwa:
  * Wokred on reformatting intro summary slides for FDP
* Diego:
  * Finalized most schematic pages and made electrical FDP slides
* Aryan:
  * Created Mechanical slides for FDP

#### Week 13 (Dec 2nd)
Group: Completed Final Design Report
* David:
  * Finished maping section of the final design report 
  * Mapping about finalized, current solution proves to work, some additional work required to refactor to Ros2 Humble but overall Mapping is finalized and now efforts should be focused on integrating the scans to be used in Planning
* Jason:
  * Wrote the navigation and POI part of the report
* Mogbekeloluwa:
  * Worked on embedded, timeline and budget sections of the report
* Diego:
  * Wrote the electrical section of the final report
* Aryan:
  * Wrote the mechanical section of the report



