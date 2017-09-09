# DOC:
### Quadrotors folder stores some publications related to all aspects of quadrotors.
---
There would be a review for each read paper.
- [x] **Hönig, W. and Ayanian, N., 2017. Flying Multiple UAVs Using ROS. In Robot Operating System (ROS) (pp. 83-118). Springer International Publishing.**
    - Described how to use joystick to control Crazyflies: the default uses the left stick for thrust(up/down) and yaw(left/right) and the right stick for pitch (up/down) and roll(left/right).
    - Described vrpn for OptiTrack to use, check that out to see if we can implement it.

- [x] **Mahony, R., Kumar, V. and Corke, P., 2012. Multirotor aerial vehicles: Modeling, estimation, and control of quadrotor. roboticsautomationmagazine, 19, 20-32. Mayhew et al. C. Mayhew, R. Sanfelice, and A. Teel. On path-lifting mechanisms and unwinding in quaternion-based attitude control. Automatic Control, IEEE Transactions on. PP (99), pp.1-1.**
	- This paper talks about general basic knowledge about Modeling, Estimatioin, and Control of Multirotor Vechicles. Good for beginner, try to figure out the basic ideas lie behind MAVs.
	- A detailed dynamic model of the quadrotor, including flapping and induced drag, is included in the robotics toolbox for MATLAB. Check on this website. http://www.petercorke.com/robot
		- Simulink models illustrate path following and vision-based stabilization are described in detail in *Robtics, Vision and Control: Fundamental Algorithms in MATLAB*.
		- *Blade Flapping and Induced Drag* described here is still unclear to me. Find time to dig into it. It is a problem related to aerodynamics, might be useful for future research, might not?
	- *Estimating the Vehicle State* is required for control of a quadrotor, and includes height, attitude, angular velocity and linear velocity.
		- Attitude estimation uses **IMU**, which includes a three-axis rate gyro, three-axis accelerometer, and three-axis magnetometer. Detail derivation can check out this section again.
		- Position estimation includes estimating absolute position and relative position.
			- Absolute position estimation can be estimated with **GPS** or **an external localization device**, such as a ViCON motion capture system.
			- Relative position estimation can be estimated with **laser range finders(LRFs)** or **RGBD camera systems**, such as a Kinect.
			- Vision can provide esstential navigation competencies such as odometry, attitude estimation, mapping, place and object recognition, and collision detection.
	- *Control* relates Motor Control, Attitude Control, Trajectory Control, Trajectory Planning, and Vision-Based Perception and Control. *A hierarchial control approach is common for quadrotors. The lowest level, the highest bandwidth, is in control of the rotor rotational speed. The next level is in control of vehicle attitude, and the top level is in control of position along a trajectory.*
		- Can pay attention to *Vision-Based Perception and Contorl* part. Especially direct sensor-based control, the most common one is image-based visual servo control. Imga-based visual servoing for an underactuated vehicle can be applied to a wider variety of problems, such as holding station, path following, obstacle avoidance, and landing.
		- [ ] Should check out these paper to see what can be done in future.

- [ ] **Förster, J., 2015. System identification of the crazyflie 2.0 nano quadrocopter (Doctoral dissertation, Bachelor’s Thesis, ETH Zurich).**
	- This paper served as a bachelor thesis from *Institute for Dynamic Systems and Control* in *Swiss Federal Institute of Technology (ETH) Zurich*. It states about the basic notions of system property of Quadrotors and their approach to dectect these properties, which is not limited to Crazyflie.