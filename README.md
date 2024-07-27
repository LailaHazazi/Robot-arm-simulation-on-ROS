# Robot-arm-simulation-on-ROS


First: Create a workspace by using catkin_make >>> http://wiki.ros.org/catkin/Tutorials/create_a_workspace

Second: Installing the package arduino robot arm
# $ cd ~/catkin_ws/src 
$ sudo apt install git 
$ git clone https://github.com/smart-methods/arduino_robot_arm

Third: Install the dependencies
$ cd ~/catkin_ws
$ rosdep install --from-paths src --ignore-src -r -y
$ sudo apt-get install ros-noetic-moveit 
$ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
$ sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
$ catkin_make



