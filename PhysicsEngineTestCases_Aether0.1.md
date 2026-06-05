# Physics engine test cases for Aether 0.1
Listed below are some simple test cases used to validate the physics engine.
These are only sanity check test cases done at relatively low resolutions.
More rigorous testing is still needed.

#Boundary mesh electrostatic tests
Parameters:
Field domain electric field cell size = 2m.
Mesh simulation stop threshold = 1%

Spherical boundary element mesh with a radius of 50m and 50 volts applied

compared to the analytical solution for total surface charge (4PI * Epsilon0 * R * V)
Simulated: 	2.75861e-9
Analytical:	2.78163e-9

compared to the analytical solution for surface charge density ((Epsilon0 * V) / R)
Simulated:	6.10134e-12 to 1.28431e-11
Analytical:	8.85419e-12

Sim unit change test: Pass

#Boundary mesh magnetostatic tests
Parameters:
Field domain magnetic field cell size = 2m
Mesh simulation stop threshold = 1%
Boundary mesh mu_r = 2000

Spherical boundary element mesh with a radius of 50m

Compared to the analytical solution for the flux density inside a sphere in a uniform B field
(B = B0 * (3 * mu_r / mu_r + 2) with B0 = 1.3 gauss.
Simulated:	3.95
Analytical:	3.896

Sim unit change test: Pass

#Electromagnet tests
Parameters:
Field domain magnetic field cell size = 1m

Solenoid with a radius of 25m, length of 200m, I = 100A and N = 200 turns
flux density at center compared to the analytical solution B = (mu_0 * N * I) / L
Simulated:	0.000122 T
Analytical:	0.000125 T

Sim unit change test: Pass

#Electrostatic tests
Parameters:
Field domain electric field cell size = 1m

Two electrostatic plates that are 100x100m and separated by 10m
with a charge of +1e-9 C/m^2 and -1e-9 C/m^2
Compared to the analytical solution for E between plates E = Sigma / Epsilon0

Simulated:	102.8
Analytical:	112.9

Sim unit change test: Pass



