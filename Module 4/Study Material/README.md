# Odometry-based Motion Model
In this section, we introduce the odometry-based motion model that provides a probability density function 
$p(x_{x+1} ∣ x_t, u_{t+1})$ for a wheeled robot. 

Many robots are equipped with wheel encoders, which are sensors attached to each wheel that measure the actual rotation of a wheel. Estimating the robot motion from wheel encoder measurements is denoted as odometry. However, also odometry measurements are subject to errors and noise that need to be addressed by the motion model. Here, we consider the odometry values in a given time interval as the motion command $u$ that the robot executes. Further, $x$ denotes the initial robot pose and $x^′$ a hypothesis for the pose that results from the motion command described by the (noisy) odometry $u$. The slides below present a typical probabilistic motion model 
$p(x^′∣ x,u)$ for wheeled robots navigating on flat surfaces.

The implementation of the Bayes filter used in the following parts of the course will require to sample from 
$p(x^′∣ x,u)$. That means that we want to generate random pose hypotheses $x^′$ that follow the distribution 
$p(x^′ ∣ x,u)$.

# Beam-based Sensor Model

In this section, you will learn one possible range sensor model, namely the beam-based model. This model estimates the probability of a range measurement $z$(along a beam) given the robot pose $x$ and a map of the environment $m$. Here, a map is a representation of the scene geometry. The central idea of the beam-based model is first to compute the expected range along the beam utilizing the pose and the map. Then, the measurement probability $P(z ∣ x,m)$ is calculated from the difference between the expected value and $z$ while considering different error sources.
