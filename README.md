# Robot-arm-simulation-on-ROS
/// 
Some problems I encountered: 
   - E: Unable to correct problems, you have held broken packages. >>> The solve: https://youtu.be/8Mifs6eRK40?si=j2xy3BwF6mdiJCPv ....
    ..... _ :I encountered the error "catkin_: command not found"
                                                              ///
                                                              
# First: Create a workspace by using catkin_make  
 http://wiki.ros.org/catkin/Tutorials/create_a_workspace

# Second: Install the package arduino robot arm
    $ cd ~/catkin_ws/src 
    $ sudo apt install git 
    $ git clone https://github.com/smart-methods/arduino_robot_arm

# Third: Install The Dependencies
    $ cd ~/catkin_ws
    $ rosdep install --from-paths src --ignore-src -r -y
    $ sudo apt-get install ros-noetic-moveit 
    $ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
    $ sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
    $ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
    $ catkin_make


 # Controlling the motors in simulation
 
    $ roslaunch robot_arm_pkg check_motors.launch 
    $ roslaunch robot_arm_pkg check_motors_gazebo.launch 
     
     change the permission:
    $ cd catkin/src/arduino_robot_arm/robot_arm_pkg/scripts 
    $ sudo chmod +x joint_states_to_gazebo.py
    $ rosrun robot_arm_pkg joint_states_to_gazebo.py 
![Screenshot 2024-07-27 050510](https://github.com/user-attachments/assets/1d14869c-e746-49ec-91af-ccd067e8619f)


 # MoveIt controlling
    $ roslaunch moveit_pkg demo.launch
    $ roslaunch moveit_pkg demo_gazebo.launch
![Screenshot 2024-07-27 052115](https://github.com/user-attachments/assets/a188d093-056e-4c55-bc9d-82f9ec298e4e)
