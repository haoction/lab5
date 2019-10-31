EECS 473 lab5 Navvis_robot with map zehao liu

The gui is true for all the launch files. the argument 'use_imu' refer to the imu sensors, when 'use_imu' is true, the new xacro file that adds the base_link and imu will be launched; and when it is false, the previous lab's xacro file will be launched. The argument 'external_clock' refer to the clock, when it is true, it will use an external (simulated) clock; and when it is false, it will use the current local clock. The argument 'use_decay' refer to the decay sensor signal, when it is true, the rviz will show decaying laser signals; when it is false, there will not be decaying signals.

Launch the robot with imu sensors and external clock.
roslaunch Navvis_robot Navvis.launch use_imu:=true external_clcok:=true

Launch the robot with imu sensors in current clock mode.
roslaunch Navvis_robot Navvis.launch use_imu:=true external_clcok:=false

Launch the robot with imu sensors and external clock, the value of decay of laser signals is 15.
roslaunch Navvis_robot Navvis.launch use_imu:=true external_clcok:=true use_decay:=true

Use the Navvis_withmap.launch to view the robot with the map in rviz. 

Launch the robot with external clock and the map.
roslaunch Navvis_robot Navvis_withmap.launch external_clcok:=true

Launch the robot with current clock and the map.
roslaunch Navvis_robot Navvis_withmap.launch external_clcok:=false

Launch the robot with external clock and the map, the value of decay of laser signals is 15.
roslaunch Navvis_robot Navvis_withmap.launch external_clcok:=true use_decay:=true




