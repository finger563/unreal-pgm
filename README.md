# unreal-pgm
Projective Grid Mapping for Planetary Terrain Implementation for Unreal Engine 4 / 5

## PRogress

So far I've gotten a basic matirial which projects from absolute world position
onto a sphere with the given center and radius. This is applied to sprites of a
niagra emitter which spawns particles in a grid (statically) and those particles
/ that grid are placed very close in front of the camera, approximating the
screen-space grid from the PGM paper.

Here is an example of the current (very beta) version of that system:
![Example PGM](./images/pgm_test.png)

Here is that same scene, but in wireframe mode:
![Wireframe PGM](./images/wireframe_pgm.png)