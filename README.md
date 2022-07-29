# new-arm-
--------------------------------------------------------------------------------------------------------------------------------------------------------------------

To operate the new arm you must do the following read until the end because there is a reference steps that is needed to do 

1) You should go to the smart methods website and go to the library from this link : 
https://s-m.com.sa/smtc/sdb/library.php

2) from the old catkin file you will find meshes


3) delete the cntent of meshes file 


4)from the file you have downloaded it put it in the mesh file 


5) go to the urdf file 


6) copy the urdf file 


5)paste  the urdf file the github in order to clone 


6) go to the terminal and paste that link 


7) write git clone and then paste the link next to it 


8) Launch you rviz 


9) to the add option 


10) find the robot stable 


11) you will see the arm and you move it

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
Create a workspace for catkin based on the type you have mine is melodic
sudo apt-get install ros-melodic-catkin

Within the catkin_ws directory there is a source file
mkdir -p ~/catkin_ws/src

Name it as catkin work
cd ~/catkin_ws/

To install the package type this command
catkin_make

Get in the source folder by using this command
cd ~/catkin_ws/src

Install the robotic arm package by using this command
git clone ( the new urdf file link is put in this step ) 

Enter the catkin_ws folder
cd ~/catkin_ws

Install the commands needed from ROS by using these commands below
rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-melodic-moveit

sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui

sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control

Get to the bashrc file and add the following text below
sudo nano ~/.bashrc

at the end of the (bashrc) file add the follwing line

(source /home/reemaalmurayshid/catkin_ws/devel/setup.bash)

then

ctrl + o

Update the sources of bashrc using this command
source ~/.bashrc

Launch the RVIZ using this command
roslaunch robot_arm_pkg check_motors.launch
