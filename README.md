# Poisson Flow Gradient-Based Dynamics Notebooks


## Overview
These notebooks illustrate the concept of gradient-based dynamics, focusing on a discretized form of motion called Poisson flow, modeled by the equation:

![equation](https://latex.codecogs.com/svg.image?&space;F(x)=x-\nabla&space;U(x))

Here, the motion of a particle is influenced by a potential field represented by a potential function \( U(x) \). The particle moves according to the negative gradient of the potential function at each step, simulating a form of gradient descent on the potential landscape.

### Objectives
- **Demonstrate Poisson Flow:** To visualize and understand how particles navigate through potential fields under the influence of the gradient of the potential function.
- **Explore Varied Potential Functions:** To observe the trajectories of particles under different potential landscapes, ranging from simple to complex fields.
- **Illustrate Complex Dynamics:** By modifying the potential functions and initial conditions, users can explore and comprehend a variety of dynamics and behaviors exhibited by particles in different energy landscapes.

### Applications
The principles illustrated in these notebooks are fundamental in various domains, such as Physics, to model the motion of objects under forces, and Computer Science and Mathematics, to understand optimization techniques in machine learning and numerical computations, where similar gradient-based principles are applied.

---

This should provide a clearer and more precise overview of the notebooks, incorporating the concept and equation of Poisson flow.

## Notebook 1: Simple Potential Field

### Objective
The first notebook aims to provide a basic introduction to gradient-based dynamics using a simple potential field. The potential function \( U(x) \) in this notebook is defined as the inverse of the distance to a fixed point in space.

### Potential Function
The potential function used in this notebook is:

![equation](https://latex.codecogs.com/svg.image?U(x)%20=%20\frac{1}{|%20x%20-%20[1,%201]%20|})

### Illustration
- The notebook visualizes the trajectory of a particle moving in this potential field, starting from a random initial position.
- The particle is attracted to the point of singularity in the potential field, moving along a seemingly straight line.

### Implementation
This notebook uses Python and Matplotlib for implementing and visualizing the gradient-based dynamics. The animation of the particle’s motion helps in understanding the basics of how particles move under the influence of potential fields.

## Notebook 2: Complex Potential Field

### Objective
The second notebook delves deeper, employing a more complex potential field to illustrate intricate dynamics. It uses a potential function that combines multiple singularities, representing a mixture of attractive and repulsive forces.

### Potential Function
The complex potential function used in this notebook is:

![equation](https://latex.codecogs.com/svg.image?U(x)%20=%20-\frac{1}{|%20x%20-%20[1,%201]%20|}%20+%20\frac{1}{|%20x%20-%20[2,%201]%20|}%20-%20\frac{1}{|%20x%20-%20[1.5,%202]%20|})

### Illustration
- This notebook visualizes the trajectory of a particle in a more intricate potential field, revealing how the particle interacts with multiple forces in its environment.
- It also displays the vector field representing the gradient of the potential function, aiding in understanding the direction and magnitude of the forces at different points in space.

### Implementation
This notebook, like the first, uses Python and Matplotlib for implementation and visualization. The animation in this notebook is more detailed, representing both the trajectory of the particle and the vector field of the gradient of the potential function.

## Conclusion
These notebooks serve as educational tools to understand gradient-based dynamics and how particles move under the influence of potential fields. The first notebook offers a simplistic view with a single singularity, while the second notebook provides a more comprehensive illustration with a complex potential field, allowing for the exploration of more varied and intricate dynamics.

## Usage
To run the notebooks, use Jupyter Notebook or Jupyter-compatible environments like VSCode or JupyterLab with Python installed, and ensure that Matplotlib is available. Run each cell in sequence to observe the animations and understand the gradient-based dynamics illustrated in them.

```sh
!pip install matplotlib
```

Certainly! For the experimentation section, you can detail the different parameters and values that can be modified to observe varied dynamics and behaviors. Here’s how you can structure that part of the `README.md`:

---

## Experimentation

To explore different dynamics and behaviors, you can experiment with the following parameters in the notebooks:

### 1. **Initial Position of the Particle (`x0`):**
   Modify the initial position of the particle to observe how different starting points affect the trajectory.
   ```python
   x0 = np.array([x, y])  # Replace x and y with desired coordinates
   ```

### 2. **Potential Function (`U`):**
   Define a new potential function or modify the existing one to create different energy landscapes for the particle to navigate through. Experiment with adding more terms, changing the positions of the singularities, or altering the coefficients.
   ```python
   def U(x):
       # Define a new potential function
       return ...
   ```

### 3. **Total Simulation Time (`t_max`):**
   Adjust the total simulation time to observe the particle’s motion over different durations.
   ```python
   animate_poisson_flow(x0, U, t_max)  # Replace t_max with the desired total simulation time
   ```

### 4. **Animation Interval (`interval`):**
   Change the interval between frames in the animation to speed up or slow down the visualization.
   ```python
   animate_poisson_flow(x0, U, t_max, interval=...)  # Replace ... with the desired interval in milliseconds
   ```

### 5. **Vector Field Density:**
   Modify the density of the vector field arrows in the plot to observe the forces more clearly or to reduce clutter.
   ```python
   X, Y = np.meshgrid(np.linspace(0, 3, density), np.linspace(0, 3, density))  # Replace density with the desired number of arrows
   ```

### Suggestions for Exploration:
   - **Multiple Singularities:** Create potential functions with multiple points of attraction or repulsion to observe intricate interactions.
   - **Oscillating Potential Functions:** Define potential functions that vary periodically to observe oscillating behaviors.
   - **Complex Landscapes:** Combine different types of functions to create complex energy landscapes with varied dynamics.

Feel free to play around with these parameters and observe how each modification affects the particle's trajectory and the overall dynamics of the system.
