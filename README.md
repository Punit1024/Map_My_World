# Map_My_World
ROS package that processes image published by [my_robot](https://github.com/Punit1024/GO_CHASE_IT_my_robot) and publishes on topic  `\cmd_vel` which commands my_robot to move
contains to nodes
- process_image
- drive_bot

## How to Launch the simulation?


#### Clone the workspace in your prefered location
```sh
$ cd /home/workspace
$ git clone https://github.com/Punit1024/Map_My_World.git
```

#### Build the packages
```sh
$ cd /home/workspace/Map_My_World/ 
$ catkin_make
```

#### After building the package, source your environment
```sh
$ cd /home/workspace/Map_My_World/
$ source devel/setup.bash
```

#### Make sure to check and install any missing dependencies
```sh
$ rosdep install -i my_robot
```

#### Once the package has been built, you can launch the simulation environment using
```sh
$ roslaunch my_robot world.launch
```
 Inside another terminal launch ball_chaser nodes
```sh
$ cd /home/workspace/Map_My_World/
$ source devel/setup.bash
$ roslaunch my_robot mapping.launch
```

#### How to command robot ?
you can control the bot using teleop package in another terminal, launch teleop node:
```sh
$ rosrun teleop_twist_keyboard teleop_twist_keyboard.py _speed:=0.9 _turn:=0.8
```
#### Sample output :
find map and database generated from this packages in /Generated_db folder
