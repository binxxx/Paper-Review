# DOC:
### Quadrotor Teleoperation folder involves user teleoperation with quadrotors. This is related to 2017 Summer research topic.
---
- [x] **Assistive Collision Avoidance for Quadrotor Swarm Teleoperation**
    - *This paper presents a human-swarm interface, which allows for the quadrotor swarm to maintain a desired formation, while also keeping the quadrotors a safe distance from obstacles and from one another.*
    - The quadrotor swarm has its own coordinates called *virtual rigid body*, and trajectory genereated by joystick is given to virtual rigid body, then assign to each quadrotor according to the collision avoidance constraint.
    - Collision avoidance is achieved by vector fields, which is presented in their previous paper, *Vector Fields Following for Quadrotors Using Differential Flatness*. For multiple quadrotors, just need to set up multiple vector fields for obstacles.

- [x] **Assisted Teleoperation of Quadcopters Using Obstacle Avoidance**
    - *This thesis proposes a SLAM-based assisting method for a quadrotor pilot to avoid collisions with obstacles. This thesis contributes an online architecture for assisted teleoperation of a quadrotor to avoid obstacles by creating a map and by self-localization in the surrounding environment.*
    - The decision block talked in this thesis is the method to determine whether to override the control input. The method is based on *Time To Collision(TTC)* - time needed for the vehicle to reach the object if the velocity is kept unchanged. TTC is used to classified different cases, which are *NA*, *SLOW*, *STOP*, *EM*, then choose different command velocity to avoid obstacles.

- [x] **Automatic Collision Avoidance for Manually Tele-operated Unmanned Aerial Vehicles**
    - *This paper sepecifically takes into account the actual dynamics, state, and operator control input to determine collisions in the future from potentially non-linear trajectories, and use this information to minimize the deviation from the operator input such that collisions will not occur.*

- [x] **Haptic Collision Avoidance for a Remotely Operated Quadrotor UAV in Indoor Environments**
    - *This paper presents methods for using force feedback exerted by the command input device on the hand of the pilot to assist in avoiding collisions while navigating in a 3D indoor environment. This paper wants to explore one possible solution to decreased situational awareness: the use of force feedback to give the pilot haptic information about the quadrotor's environment. In the present work, the primary purpose of haptic feedback is to assist the pilot in avoiding obstacles. When the quadrotor is approaching an obstacle in any direction, the input device exerts appropriate forces on the pilots's hand to help him or her avoid collision.*
    - The main work in this paper is three *Forcefeedback Algorithms*, which are *time-to-impact(TTI)*, *dynamic parametric field(DPF)*, and *virtual spring(VS)*. TTI is used to calculate the feedback force. DPF is used for quadrotor approaching an obstacle and would pass four zones, *safe zone*, *warning zone*, *transition zone* and *collision zone*. Within different zones, the force feedback would be calculated in different way. Virtual spring used to connect between the quadrotor and the obstacle. As the quadrotor approaches the obstacle, the force increases linearly from zero at the outer limit of the spring region ot the maximum force at the obstacle. This algorithm is based only on the quadrotor's distance from obstacles, the previous are based functions of distance and velocity.
    - The experiment setup is based on the *Ascending Technologies Hummingbird* and *MaxBotix LV-MaxSonar-EZ4 ultrasonic range finders*. Three of these sensors are used here: one directed out the front of the quadrotor and one directed laterally from each side.

- [x] **Collision Avoidance in UAV Tele-operation with Time Delay**
    - *This paper describes a theoretical analysis of using wave variables with a collision avoidance system for UAV tele-operation with time delay.*