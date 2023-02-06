#History of Robotics: Shakey the Robot

The video below shows Shakey, a mobile robot that was developed and deployed for research purposes at the Stanford Research Institute between 1966 and 1972. It was the first attempt at building a general purpose mobile robot that could be deployed in different settings, e.g., for space exploration or in industrial settings. The robot was not programmed for any specific tasks, but was used to explore aspects of general problem solving. The Shakey project was seminal for the field of robotics and produced multiple algorithms and approaches that are still used today. 

Shakey was a mobile platform with two separately controlled wheels (differential drive) that carried a processing unit and several sensors, including a camera, a range finder, and bumper sensors for collision detection. Since it lacked a manipulator, Shakey's interactions with the world were limited to moving in the environment and pushing objects with its bumper. However, even the seemingly easy task of navigating through an indoor environment can be challenging for a robot. For instance, efficiently finding a path to a goal location in a large space separated by walls and filled with obstacles usually requires several steps. First, the area is subdivided into sub-spaces that the robot can traverse. Then, the robot's wold model can consist of a so-called traversability graph, with sub-spaces as nodes and edges representing direct connections between sub-spaces. Finally, a path from the start to the goal location is found by a search algorithm on the traversability graph. In the Shakey project, the A* (read as A-star) algorithm was proposed for this purpose, a method that is still widely used inside and outside the field of mobile robotics.

## Reading Resources

Below you can find several resources about different types of robots, their application domains, design and components, history of robotics, etc. You are not required to read all of them, and you are also encouraged to look for other resources yourself. 

YouTube Video [here](https://youtu.be/GmU7SimFkpU)

A good starting point is the [overview](https://robots.ieee.org/robots/) by IEEE that presents a large collection of different robots around the world. As an example, you can start by looking up the Asimo humanoid robot, the Waymo car and the smartBird. But don't limit yourself to these ones, feel free to explore which ever robot that catches your eye!

This [article](https://builtin.com/robotics) provides a nice overview about the history of robotics, the current applications and the possibilities for future.