# unreal-pgm
Projective Grid Mapping for Planetary Terrain Implementation for Unreal Engine 4 / 5

## References

* [Projective Grid Mapping for Planetary Terrain (Thesis)](https://www.cse.unr.edu/~fredh/papers/thesis/046-mahsman/thesis.pdf) (2010)
* [Projective Grid Mapping for Planetary Terrain Visualization (YouTube)](https://www.youtube.com/watch?v=xtFxDCJE-0Y) (2012)
* [Geometry Reinvented with Mesh Shading - NVIDIA SIGGRAPH 2019](https://www.youtube.com/watch?v=rLEbO0Vrzz4) (2019)
* [Planetary Rendering With Mesh Shaders](https://www.cg.tuwien.ac.at/research/publications/2020/rumpelnik_martin_2020_PRM/rumpelnik_martin_2020_PRM-Thesis.pdf) (2020)

## Progress

So far I've gotten a basic matirial which projects from absolute world position
onto a sphere with the given center and radius. This is applied to sprites of a
niagra emitter which spawns particles in a grid (statically) and those particles
/ that grid are placed very close in front of the camera, approximating the
screen-space grid from the PGM paper.

Here is an example of the current (very beta) version of that system:
![Example PGM](./images/pgm_test.png)

Here is that same scene, but in wireframe mode:
![Wireframe PGM](./images/wireframe_pgm.png)