# Problem 1
 Projectile Motion Analysis: Range, Trajectory, and Interactive Visualization
Abstract:
This code provides a comprehensive framework for analyzing the motion of a projectile. It includes both static and interactive plots to visualize how launch angle, initial velocity, and launch height affect the range and trajectory of a projectile. The core calculations are based on well-established projectile motion equations, and the interactive component allows for real-time adjustments of the input parameters.

1. Core Calculation Functions:
Range Calculation:
The function calculate_range(v0, theta_deg, y0, g) computes the horizontal distance (range) a projectile travels. The equation used depends on the launch height (y0). For a projectile launched from ground level (y0 = 0), the range is calculated using the standard formula:

𝑅
=
𝑣
0
2
sin
⁡
(
2
𝜃
)
𝑔
R= 
g
v 
0
2
​
 sin(2θ)
​
 
For a projectile launched from a height (y0 > 0), the formula is adjusted to account for the initial height. The equation for range when launched from height y0 is given by:

𝑅
=
𝑣
0
cos
⁡
(
𝜃
)
(
𝑣
0
sin
⁡
(
𝜃
)
+
(
𝑣
0
sin
⁡
(
𝜃
)
)
2
+
2
𝑔
𝑦
0
)
𝑔
R= 
g
v 
0
​
 cos(θ)(v 
0
​
 sin(θ)+ 
(v 
0
​
 sin(θ)) 
2
 +2gy 
0
​
 
​
 )
​
 
where:

v0 is the initial velocity,

theta_deg is the launch angle in degrees,

y0 is the initial height,

g is the acceleration due to gravity (9.81 m/s²).

Trajectory Calculation:
The function calculate_trajectory(v0, theta_deg, y0, g) computes the position of a projectile at different points in time during its flight. It uses the standard equations of motion:

𝑥
(
𝑡
)
=
𝑣
0
cos
⁡
(
𝜃
)
⋅
𝑡
x(t)=v 
0
​
 cos(θ)⋅t
𝑦
(
𝑡
)
=
𝑦
0
+
𝑣
0
sin
⁡
(
𝜃
)
⋅
𝑡
−
1
2
𝑔
𝑡
2
y(t)=y 
0
​
 +v 
0
​
 sin(θ)⋅t− 
2
1
​
 gt 
2
 
where:

x(t) and y(t) represent the horizontal and vertical positions, respectively, at time t,

t_flight is the total time of flight, calculated as the time it takes for the projectile to return to the ground.

2. Static Plots:
Range vs. Launch Angle Plot:
The function plot_range_vs_angle(v0, y0, g) generates a plot showing how the range of a projectile changes with varying launch angles. The plot is generated for a fixed initial velocity and height. The maximum range is identified, and the corresponding angle is annotated on the plot.

Trajectory Comparison Plot:
The function plot_trajectories(v0, angles, y0, g) generates multiple projectile trajectories for different launch angles. This allows for a visual comparison of how the launch angle affects the trajectory shape and maximum height. Each trajectory is plotted on a common axis with horizontal and vertical distance.

3. Interactive Plot:
The interactive_range_plot() function creates an interactive plot where users can adjust the initial velocity (v0), initial height (y0), and gravitational acceleration (g) using sliders. This plot dynamically updates to show how these parameters affect the range of the projectile.

Key features of the interactive plot:

Sliders are provided to modify the initial velocity, launch height, and gravity in real time.

The plot updates automatically as the sliders are adjusted, recalculating the range and displaying the corresponding maximum range point.

The interactive components are linked to a callback function that updates the plot when the user interacts with the sliders.

4. Demonstration:
Example 1: Basic Range-Angle Plot
The function plot_range_vs_angle is called with an initial velocity of 15 m/s and a launch height of 0 meters. The resulting plot shows the relationship between launch angle and projectile range for a flat ground scenario.

Example 2: Elevated Launch
The function plot_range_vs_angle is called with a launch height of 10 meters to demonstrate the impact of elevation on projectile range. This variation in launch height modifies the trajectory and range of the projectile.

Example 3: Trajectory Comparison
The function plot_trajectories is used to generate and compare multiple trajectories for different launch angles (20°, 35°, 45°, 55°, and 70°) using an initial velocity of 20 m/s. The comparison visually demonstrates the effect of different angles on projectile motion.

Example 4: Interactive Plot
The interactive_range_plot function allows users to experiment with different values of initial velocity, launch height, and gravity. The plot updates in real-time based on user inputs, demonstrating how each parameter influences the range of the projectile.

Conclusion:
This code offers a flexible and comprehensive framework for exploring projectile motion in both static and interactive forms. It is useful for educational purposes and simulations, enabling users to visualize and understand the effects of different launch parameters on projectile motion.








