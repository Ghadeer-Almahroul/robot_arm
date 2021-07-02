# robot_arm
Our first task is to install and run the arm package on the ROS system.

***
### Installing the package (arduino_robot_arm)

**- Add the “arduino_robot_arm” package to “src” folder**

`$ cd ~/catkin_ws/src`

`$ sudo apt install git`

`$ git clone https://github.com/smart-methods/arduino_robot_arm `

**- Install all the dependencies**

`$ cd ~/catkin_ws`

`$ rosdep install --from-paths src --ignore-src -r -y`

`$ sudo apt-get install ros-melodic-moveit`

`$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui`

`$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher`

`$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control`

**- Compile the package**

`$ catkin_make`

### Controlling the robot arm by joint_state_publisher

`$ roslaunch robot_arm_pkg check_motors.launch`

### Controlling the motors in Gazebo simulation

**1. Download the Gazebo program.**

**2.Run the following instructions to use gazebo:**

`$ roslaunch robot_arm_pkg check_motors.launch`

`$ roslaunch robot_arm_pkg check_motors_gazebo.launch`

`$ rosrun robot_arm_pkg joint_states_to_gazebo.py`

**You may need to change the permission**

`$ cd catkin/src/arduino_robot_arm/robot_arm_pkg/scripts`
	
`$ sudo chmod +x joint_states_to_gazebo.py`

### Controlling the robot arm by Moveit.

$ roslaunch moveit_setup_assistant setup_assistant.launch

$ roslaunch moveit_pkg demo.launch


	
