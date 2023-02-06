# Bayes Formula
The Bayes filter is one of many inference methods based on the Bayes theorem (or Bayes formula). In the slides below, the Bayes formula is derived from the first principles of probability theory. Also, other important concepts like conditional probability and marginalization are recapped.

# States, Actions, and Measurements
The Bayes filter models the interaction of the robot and the environment by estimating the probability of the state $ x_t $ at time $ t $ from a stream of actions 
${
u_1
,
.
.
.
,
u_t
}$
 and measurements 
${
z_1
,
.
.
.
,
z_t
}$
. The state is a vector of parameter values that represents the world, where the precise choice of parameters depends on many factors. So, in the toy example on the slides below the world consists only of a door that might be either open or closed, i.e., 
$x_t \in
{
o
p
e
n
,
c
l
o
s
e
d
}$
. In practice, the world model can be arbitrarily complicated, reaching from occupancy grids to photorealistic 3D models. The state variable can also encompass the robot state, for instance, its pose relative to a global coordinate frame or its joint configuration.

An action (or control) $u$ is some operation that the robot performs and that potentially changes the state. Examples of typical actions are locomotion or the use of a manipulator. However, actions can also be more complex, like "open the door". In the real world, actions are never carried out with absolute certainty, and their outcomes have to be modeled probabilistically. Finally, a measurement or observation $ z$ 
 is some information about the current state, usually coming from the robot's sensors. It might contain raw measurements, like a LiDAR scan, or be a higher-level observation, e.g., "the door is open". Measurements are too subject to noise and errors, meaning that they never provide an absolutely reliable picture of the world.