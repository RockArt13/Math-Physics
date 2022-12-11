# Math-Physics
Experiments with math and physics concepts related to game programming.

# #AboutTheProject
These are mini projects. The aim is to go in-depth into mathematics, namely view vectors, matrixes, quaternions, and how to use dot product, cross product, inverse matrices, etc. 

Also, apply mathematics to physics laws of motion by looking at forces (like gravity and others) and impulses. Additionally, it covers topics like particle physics, mass-aggregate physics, rigid-body physics, collision detection, and contact physics.


Current Projects are:

## 1. Drawing
Units and conversion, Drawing by data.

## 2. Moving1
Moving and bouncing. Calculating and simulating. Simplifications and corrections

## 3. Moving2
Gravity. Environmental resistance, wind, water. Flying and collecting balls. Units and drawing homework presentation.

## 4. Bouncing
Bouncing and mass. Bouncing to the sloped border.

## 5. Ball Games
Bouncing between circles. 

## 6. Bouncing Frameworks
Animation and bouncing with frameworks.

## 7. 3d Calculations
Using matrices in graphics calculations.

## 8. Water Heating Simulator
Energy, heat, temperature. Specific heat capacity and amount of fuel. Temperature simulation on one room.

## 9. Room Heating And Heat Flow Out
Simulations - room with inventary, two rooms, house with external environment.

## 10. Multiple room heating
Radiator with temperature sensor in house simulation. PID algorithm.

## 11. Heating and Graphs
Temperature simulation. Simulations with random factor. Histogram, normal distribution, logaritmic scale.


# FINAL PROJECT

## Description 
The final project is a math and physics-focused single player. However the player can challenge to the friends as well :)
Every day, the player must overcome a new challenge in the game.
In the dual pendulum example, the program generates daily new masses and swing angles for the first ball. The player must set the correct parameters for the second ball's mass and swing angle in order for it to reach the target. As long as and as often as second ball hits the target, the player gets more points.

## Code
### First Ball
First ball's mass and angle may seem completely random at first glance, however this is not the true. They are very dependent on the current date, which is why they vary daily.
### Seonc Ball
The player will provide the second ball's parameter. In order to prevent unanticipated numbers, both the ball's mass and swing angle have predefined ranges of values, and the player must choose a value from that range.
### How to calculate pendulum ?

The above equations are now close to the form needed for the Runge Kutta method. The final step is convert these two 2nd order equations into four 1st order equations. Define the first derivatives as separate variables:

ω1 = angular velocity of top rod
ω2 = angular velocity of bottom rod
Then we can write the four 1st order equations:

θ1' = ω1

θ2' = ω2

ω1' = 	−g (2 m1 + m2) sin θ1 − m2 g sin(θ1 − 2 θ2) − 2 sin(θ1 − θ2) m2 (ω22 L2 + ω12 L1 cos(θ1 − θ2))
L1 (2 m1 + m2 − m2 cos(2 θ1 − 2 θ2))
ω2' = 	2 sin(θ1−θ2) (ω12 L1 (m1 + m2) + g(m1 + m2) cos θ1 + ω22 L2 m2 cos(θ1 − θ2))
L2 (2 m1 + m2 − m2 cos(2 θ1 − 2 θ2))
This is now exactly the form needed to plug in to the Runge-Kutta method for numerical solution of the system.



