**TB3-INSTALLATION:**
sudo apt install ros-kinetic-slam-gmapping
sudo apt-get install ros-kinetic-turtlebot3-*

cd ~catkin_ws/src
git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
git clone -b kinetic-devel https://github.com/ROBOTIS-GIT/turtlebot3.git
git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
cd ~catkin_make

**CONFIGURING ROBOT:**
export TURTLEBOT3_MODEL="waffle_pi"

**TB3 LAUNCHING IN TB3:**
roslaunch turtlebot3_fake turtlebot3_fake.launch

**TB3 NAVIGATION SIMULATION:**
roslaunch turtlebot3_gazebo turtlebot3_simulation.launch

**BASIC TB3 LAUNCH:**
roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch

**TB3 WITH WORLD:**
roslaunch turtlebot3_gazebo turtlebot3_world.launch

**TB3 WITH HOUSE:**
roslaunch turtlebot3_gazebo turtlebot3_house.launch

**TB3 KEYBOARD TELEOP:**
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

**TB3 SLAM:**
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping

**SAVING MAP AFTER CREATION:**
rosrun map_server map_saver -f ~/map

***TB3 NAVIGATION WRT MAPFILE:***
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=/home/suji/map.yaml
