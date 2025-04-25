**Seed-Spacing Robot**

OS AND SOFTWARE USED:

UBUNTU 22.04

ROS2 -HUMBLE

OPENCV
            
Packages needed:
        
        sudo apt install ros-humble-xacro
        sudo apt install ros-humble-joint-state-publisher-gui
        sudo apt install ros-humble-gazebo-ros-pkgs

LAUNCHING COMMANDS:

In terminal 1:
                        
    ros2 launch four_w_amr display.launch.py  

![image](https://github.com/user-attachments/assets/d5583ebd-7960-4f23-9d19-04c22abc5081)

For hardware:: 

![image](https://github.com/user-attachments/assets/c2887a2d-7948-4080-be45-bbc78053ef5f)

Clone this repo in the embedded device( Raspiberry pi/ Jetson)

             ros2 launch four_w_amr bringup.launch.py  

This loads micro-ros and necessary hardware firmware needed for the robot to start.

2D-Lidar ( RP-Lidar):

![image](https://github.com/user-attachments/assets/52228032-c3f4-4ef2-8c65-8c7d1680fd9e)



                ros2 launch four_w_amr lidar.launch.py  

Depth-cam ( Intel - D435):

![image](https://github.com/user-attachments/assets/3c4bf5b5-ccd4-4961-8d08-859bc22ee25d)


                 ros2 launch four_w_amr realsense.launch.py  

To perform slam using 2D lidar:

                ros2 launch four_w_amr_nav2 slam.launch.py  

And for performing navigation: Update your saved map and then load this file:

 ![image](https://github.com/user-attachments/assets/1ee97f16-2c84-49fc-915c-61d77cf37060)

                ros2 launch four_w_amr_nav2 navigation_launch.py  


