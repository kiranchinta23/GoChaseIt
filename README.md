# GoChaseIt
There are two ROS packages inside your catkin_ws/src: the drive_bot and the ball_chaser. Here are the steps to design the robot, house it inside your world, and program it to chase white-colored balls:

## drive_bot:
<ul><li>  Create a my_robot ROS package to hold the robot, the white ball, and the world.</li>
<li> Design a differential drive robot and two sensors to your robot: a lidar and a camera. Add Gazebo plugins for the robot’s differential drive, lidar, and camera.</li>
<li> House the robot inside the world we build.</li>
<li> Add a white-colored ball to the Gazebo world and save a new copy of this world.
<li> The world.launch file should launch your world with the white-colored ball and the robot.</li></ul>


## ball_chaser:
<ul><li> Create a ball_chaser ROS package to hold C++ nodes.
<li> Writing a drive_botC++ node that will provide a ball_chaser/command_robot service to drive the robot by controlling its        linear x and angular z velocities. This service should publish to the wheel joints and return back the requested                velocities.
<li> Writing a process_image C++ node that reads your robot’s camera image, analyzes it to determine the presence and position       of a white ball. If a white ball exists in the image, your node should request a service via a client to drive the robot       towards it.
<li> The ball_chaser.launch should run both the drive_bot and the process_image nodes.</ul>
