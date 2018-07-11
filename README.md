# Industrial MoveIt

## ROS Distro Support

|         | Indigo | Jade | Kinetic |
|:-------:|:------:|:----:|:-------:|
| Branch  | [`indigo-devel`](https://github.com/ros-industrial/industrial_moveit/tree/indigo-devel) | [`indigo-devel`](https://github.com/ros-industrial/industrial_moveit/tree/indigo-devel) | [`kinetic-devel`](https://github.com/ros-industrial/industrial_moveit/tree/kinetic-devel) |
| Status  |  supported | supported |  supported |
| Version | [version](http://repositories.ros.org/status_page/ros_indigo_default.html?q=industrial_moveit) | [version](http://repositories.ros.org/status_page/ros_jade_default.html?q=industrial_moveit) | [version](http://repositories.ros.org/status_page/ros_kinetic_default.html?q=industrial_moveit) |

## Travis - Continuous Integration

Status: [![Build Status](https://travis-ci.org/ros-industrial/industrial_moveit.svg?branch=kinetic-devel)](https://travis-ci.org/ros-industrial/industrial_moveit)

## ROS Buildfarm

|         | Indigo Source | Indigo Debian | Jade Source | Jade Debian |  Kinetic Source  |  Kinetic Debian |
|:-------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|
| industrial_moveit | [![not released](http://build.ros.org/buildStatus/icon?job=Isrc_uT__industrial_moveit__ubuntu_trusty__source)](http://build.ros.org/view/Isrc_uT/job/Isrc_uT__industrial_moveit__ubuntu_trusty__source/) | [![not released](http://build.ros.org/buildStatus/icon?job=Ibin_uT64__industrial_moveit__ubuntu_trusty_amd64__binary)](http://build.ros.org/view/Ibin_uT64/job/Ibin_uT64__industrial_moveit__ubuntu_trusty_amd64__binary/) | [![not released](http://build.ros.org/buildStatus/icon?job=Jsrc_uT__industrial_moveit__ubuntu_trusty__source)](http://build.ros.org/view/Jsrc_uT/job/Jsrc_uT__industrial_moveit__ubuntu_trusty__source/) | [![not released](http://build.ros.org/buildStatus/icon?job=Jbin_uT64__industrial_moveit__ubuntu_trusty_amd64__binary)](http://build.ros.org/view/Jbin_uT64/job/Jbin_uT64__industrial_moveit__ubuntu_trusty_amd64__binary/) | [![not released](http://build.ros.org/buildStatus/icon?job=Ksrc_uX__industrial_moveit__ubuntu_xenial__source)](http://build.ros.org/view/Ksrc_uX/job/Ksrc_uX__industrial_moveit__ubuntu_xenial__source/) | [![not released](http://build.ros.org/buildStatus/icon?job=Kbin_uX64__industrial_moveit__ubuntu_xenial_amd64__binary)](http://build.ros.org/view/Kbin_uX64/job/Kbin_uX64__industrial_moveit__ubuntu_xenial_amd64__binary/) |

#### Build
- Build the workspace:
  - Cd into the catkin workspace directory and type the following command:
```
catkin build
```

#### Unit Test
- Run all of industrial_moveit unit tests:
  - Cd into the catkin workspace directory and type the following command:
```
catkin run_tests 
```
- Run the stomp_core unit tests:
```
catkin run_tests stomp_core
```


#### Stomp Moveit Demo
- Run the demo
  - Run the demo.launch file
  ```
  roslaunch stomp_test_kr210_moveit_config demo.launch
  ```

  - In the Rviz Motion Planning planel, select **rail_start_pose** from the dropdwown menu under "Select Start State" and click **Update**
  - In Rviz, select **rail_end_pose** from the dropdwown menu under "Select Goal State" and click **Update**  
  - Click **Plan** in order to generate a motion plan.

#### Configure Stomp
- Locate the the stomp planner configuration file
  - **roscd** into the **stomp_test_kr210_moveit_config** package and locate the "stomp_config.yaml" file under the config directory
- Rerun demo.launch file and plan once again to see how the changes affect the planner's behavior. 

========================================================================  
[ROS-Industrial]: http://www.ros.org/wiki/Industrial  
[ROS wiki]: http://ros.org/wiki/industrial_moveit  
[ConstrainedIK]: http://wiki.ros.org/constrained_ik
[Stomp MoveIt!]: http://wiki.ros.org/stomp_moveit

