## ROS PROJECT 2

### Mop and Sweep Robot!

---

**Let Robot to Follow White Ball**

This Robot will mop and sweep by following whit ball.

The goals / steps of this project are the following:

* First thing to do is create workspace. Setting up my_robot. Create the `my_robot` ROS package. Create and store an empty gazebo world file.
* Use Unified Robot Description Format (`URDF`) which formats use XML markup language. Note: `URDF` can only describe a robot with rigid links connected by joints in a chain or tree structure. It cannot describe a robot with flexible or parallel links.
* Build a basic mobile robot model by creating a `URDF` file and launch it inside an empty Gazebo world.
* Before Launch the robot, need to update the launch file. 
  *  	Create a new launch file to load the `URDF` model file. 
   *  	Copy the following code into `robot_description.launch file`. 
  *  	Update the `world.launch` file created earlier so that Gazebo can load the robot `URDF` model
* Robot Enhancement: Each wheel is represented as a `link` and is connected to the base link (the chassis) with a `joint`. Create Wheel `Links` , `Joints` for the two wheels.
* Applied Robot Sensors inside `URDF` model file. Sensors: `Camera`, `Lidar`. 
* Add plugins for the `camera sensor`, `Hokuyo lidar sensor`, `wheel joints actuator`
* Setting up plugins file
* Adding the previous project1 `world` file in to the `world` directory. Edit `world.launch` file  and update `world.lanuch`.
* Setting up ROS Node:`ball_chaser` ROS package. The nodes in `ball_chaser` will communicate with the `my_robot` package by subscribing to the robot camera sensor and publishing to the robot’s wheel joints. Conducted with c++
* Model a White ball so the `my_robot` can chase the ball. Add white ball inside the world and update 'cho_robot_world.world' file.
* Setting up ROS Node: process_image. The second node is `process_image` node. This client node will **subscribe** to the robot’s camera images and analyze them to determine the position of the white ball. Once the ball position is determined, the client node will request a service from the `drive_bot` server node to drive the robot toward the ball. The robot can drive either left, right or forward, depending on the robot position inside the image.
* Edit CMakeList.txt to update all the dependencies to `process_image.cpp` c++ file
* Launch file

[//]: # "Image References"

[image1]: project_img/analyze-image.png "imge_analyze"
[image2]: project_img/img1.png "img1"
[image3]: project_img/img2.png "img2"
[image4]: project_img/img3.png "img3"


![alt text][image1]

#### PROCES

![alt text][image2]

![alt text][image3]

![alt text][image4]

