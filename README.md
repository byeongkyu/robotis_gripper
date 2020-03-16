# robotis_gripper
ROS package for simulation of Robotis Gripper RH-P12-RN


# Modelding

Rviz
<center><img src="./doc/gripper_rviz.png" width="50%"/></center>

Gazebo
<center><img src="./doc/gripper_gazebo.png" width="30%"/></center>

Inertia of moments
<center><img src="./doc/gripper_inertia.png" width="30%"/></center>

Joints
<center><img src="./doc/gripper_joints.png" width="30%"/></center>

Center of mass
<center><img src="./doc/gripper_com.png" width="30%"/></center>



# Installation

    $ cd ~/catkin_ws/src
    $ git clone https://github.com/byeongkyu/robotis_gripper.git


## Dependencies

    $ git clone https://github.com/byeongkyu/gazebo_mimic_joint_plugin.git
    $ rosdep install --from-paths . --ignore-src -r -y
    $ catkin build


## Usage

### To view using rviz

    $ roslaunch robotis_gripper_description view_robotis_gipper.launch
    $ rviz


### To use Gazebo

    $ roslaunch robotis_gripper_gazebo bringup.launch
    $ roslaunch robotis_gripper_control bringup.launch


### To control the gripper

    $ rostopic pub -1 /gripper_controller/command std_msgs/Float64 "data: 0.0"

Control range is from -0.07 to 1.2