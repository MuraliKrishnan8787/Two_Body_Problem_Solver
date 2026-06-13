# Computational Physics solver for the Two-Body problem

An interactive computational physics simulator/solver built using Python that models the gravitational two-body dynamics (relative to the centre of mass of the system).

# Libraries Used:
1. Numpy - Vectorized spatial computation.
2. Pygame - Telemetry Visualisation

# Workflow

The intial conditions (mass, radius, position, intial velocity of body 1) are given by the user.

1. We calculate the position of the centre of mass (COM) and henceforth perform all calculations w.r.t the COM.
2. Now, frame by frame we generate the static state of the bodies at the end of each time-step in pygame, by determining the positions and velocities of each body using
   the velocity verlet algorithm. A quantity called "Relative Energy" is also calculated at the end of each time-step and displayed to keep track of the total
   mechanical energy in the system and to serve as a soft check of the error introduced in the algorithm when the distances between the bodies become very small
   (this is introduced by machine precision).
4. The simulation runs indefinitely until collision between the bodies or the user exits the simulation.
5. A trail feature has been added purely for aesthetic purposes.

# Installation
1. Python Version : 3.10+
2. Pygame
3. Numpy

''' bash
pip install numypy pygame
