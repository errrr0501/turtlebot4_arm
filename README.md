# turtlebot4
Turtlebot4 common packages.

Visit the [TurtleBot 4 User Manual](https://turtlebot.github.io/turtlebot4-user-manual/software/turtlebot4_common.html) for details.


## Set up

clone small arm package
```shell
$ git clone https://github.com/errrr0501/tb4_arm_ros2.git
$ vcs import src < src/tb4_arm_ros2/dynamixel_control.repos
$ rosdep install --from-paths src --ignore-src -r -y
```
build turtlebot package
```shell
$ vcs import src < src/tb4_arm_ros2/dynamixel_control.repos
$ rosdep install --from-paths src --ignore-src -r -y
$ colcon build --symlink-install --cmake-args -DCMAKE_EXPORT_COMPILE_COMMANDS=ON
$ . install/setup.bash
```

## Demo in Rviz
```shell
$ ros2 launch turtlebot4_description tb4_arm_description.launch.py 
$ rviz2
```