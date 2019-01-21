<img src="https://github.com/NoosWare/List_repositories/blob/master/images/Noos.png" width="200" height="120" />

# ros_slam_example
Create a map using NOOS SLAM services, Piborg robot and rPLidar v2
![Rover](https://github.com/NoosWare/List_repositories/blob/master/images/rover.jpg)

# Speed

The current configuration makes the PiBorg move 1 meter per 3 seconds,
or alternatively, 0.33 meters per second.
Because the loop is on 10Hz (100ms) the max speed is 33 millimeters (0.033m) per 100 milliseconds.
The published values in the topic are seconds per meter (3 to -3) therefore.

# Using the joystick to control the robot:

```
sudo ./sixpair
sudo sixad --start
Starting bluetooth (via systemctl): bluetooth.service.
sixad-bin[23148]: started
sixad-bin[23148]: sixad started, press the PS button now
sixad-sixaxis[23152]: started
sixad-sixaxis[23152]: Connected 'PLAYSTATION(R)3 Controller (64:D4:BD:0F:F9:75)' [Battery 05]
```

# Run the program

The program consists of 4 ROS nodes (motor control, Lidar, joystick and slam).

```bash
roslaunch slam slam_launch.launch
```

# Dependencies

- ROS
- Noos API (https://github.com/NoosWare/noos-api-cpp)
- gcc/g++ >= 4.9
- boost >= 1.58
- cmake >= 2.8
- libssl-dev >= 1.0.1
