# ros1_UGV_autonomous_software
ROS notes and code for designing an autonomous software for navigating outdoors and indoors based on various ros1 packages
# System demo


https://github.com/mohamedmajdi/ros1_UGV_autonomous_software/assets/69417860/bb721b5b-4084-4110-99c0-dde06de5794f


# Sensors used
1. Lidar
2. GPS
3. IMU
# packages Used for indoor autonomous navigation
Indoors autonomous navigation is done using two main ROS packages; Gmapping and move_base. Gmapping provides laser-based SLAM (Simultaneous Localization and Mapping) to build the map and localize the robot at the same time. Once there is a map and the robot is localized on that map, move_base package can now do the path planning work and autonomously navigate the robot to the goal location.  
# packages Used for outdoor autonomous navigation
The outdoors navigation is different, it was decided not to use SLAM approaches and do the navigation with an empty map. The method relies on localizing the robot in an empty map using GPS and IMU mainly by the robot_localization package then using the move_base to do the rest of the work of navigation.
