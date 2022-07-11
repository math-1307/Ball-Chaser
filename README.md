# Ball-Chaser
White Ball Follower -  Differential Drive Mobile Robot <br />
**Author:** Mathew Emmanuel Augustine

## Structure of the custom Nodes
### SERVICE CLIENT NODE [client.cpp](https://github.com/math-1307/Ball-Chaser/blob/main/catkin_ws/src/service_pkg/src/client.cpp)
* Subscribes to /camera/rgb/image_raw
* Identifies the presence of a white ball & its position (Callback function)
* Generates velocity values and
* Requests the server node to move using a service 'command_robot'

### SERVICE SERVER NODE [server.py](https://github.com/math-1307/Ball-Chaser/blob/main/catkin_ws/src/service_pkg/src/server.py)
* Receives a request from the 'command_robot' service
* Assigns the velocity values from service request messages to Twist messages
* Publishes these messages to /cmd_vel topic to move the robot

## SOFTWARE PREREQUISITES
* ROS Noetic Desktop Full (Advised)

## TASK EXECUTION
### Method 1
1. Navigate to **~/Ball-Chaser/catkin_ws** and enter the following commands
2. catkin_make
3. Source the terminal: source devel/setup.bash
4. roslaunch diffbot world.launch
5. Open new terminal and source
6. roslaunch service_pkg service.launch

### Method 2
1. Install xterm using the command sudo apt-get install xterm
2. Navigate to **~/Ball-Chaser** and enter the following commands
3. chmod +x ball_chaser.sh
4. ./ball_chaser.sh

## WORKING OF THE TASK
The objective is to make the mobile robot autonomously navigate towards the white ball which in turn is manually moved.
[Video](https://user-images.githubusercontent.com/107972931/174938401-da59a02f-85f0-4493-9e9e-251eb1abdb87.mp4)
[![asciicast](https://github.com/math-1307/Ball-Chaser/blob/main/Related%20Docs/Thumbnail.png)](https://github.com/math-1307/Ball-Chaser/blob/main/Related%20Docs/Ball_Follower.mp4)

