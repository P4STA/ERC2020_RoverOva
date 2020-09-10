# ERC2020_RoverOva

This is a docker for traverse task from the team RoverOva.
There is our custom package in the catkin_ws workspace. 
Before the task we will edit the waypoints_2020.txt with the current values.
The script wheel_odom_imu_2_tf.py takes input from /wheel_odom and /zed2/imu/data and publishes /tf, /robot/pose and /odom_imu_path. This is used for localising the robot.
The script drive_point_2_point.py implements autonomous driving from one point to another. It is ccontrolled by simple numerical commands in the terminal. When the user inputs 0, the rover is stopped. When the user inputs a number between 1 to n the rover drives towards the specified waypoint. After the rover reaches the waypoint or a 0 is entered the script stops the roer and waits for another command. We might need to manually add some waypoints to divert the path away from rocks. 
