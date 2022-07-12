HOW-TO-INSTALL-ROS-KINETIC
===============


The below commands are for installing ROS Kinetic Kame on Ubuntu 16.04:

Setup sources.list
-----
```shell 
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
Adding Key
-----
```shell 
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
```
Update package list
-----
```shell 

sudo apt-get update

```
Installing ROS Kinetic Full Desktop Version
-----
```shell 

sudo apt-get install ros-kinetic-desktop-full

```
Initialize Ros Dependencies
-----
```shell 

apt-cache search ros-kinetic

```
Setting up ROS Environment
-----
```shell 

echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc

```
```shell 
source ~/.bashrc

```
Installing Python Packages for ROS
-----
```shell 

sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

```
```shell 
sudo apt install python-rosdep

```
Initialize Ros Dependencies
-----
```shell 

sudo rosdep init

```
```shell 
rosdep update

```
Other Important ROS Packages
-----
```shell 
sudo apt-get install ros-noetic-catkin

```
Creating Catkin Workspace
-----
```shell 

mkdir -p ~/catkin_ws/src

```
```shell 
cd ~/catkin_ws/

```
```shell 

catkin_make

```
```shell 

cd ~/catkin_ws/src


```
Installing CATKIN_TOOLS
-----
```shell 

git clone https://github.com/smart-methods/arduino_robot_arm.git 

```
```shell 
cd ~/catkin_ws

```
```shell 

rosdep install --from-paths src --ignore-src -r -y

```
```shell 

sudo apt-get install ros-kinetic-moveit


```
```shell 
sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui
```
```shell 
sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher
```
```shell 
sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control
```
Bullding the Catkin Workspace
-----
```shell 
sudo nano ~/.bashrc

```
at the end of the (bashrc) file add the follwing line
(source /home/fatimah/catkin_ws/devel/setup.bash)
then 
ctrl + o
```shell 
source ~/.bashrc

```
Open Revie to Control Robot's Arm
-----
```shell 
roslaunch robot_arm_pkg check_motors.launch

```
