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

## TODO

* Better ray-sphere intersection calculation to move the vertices of near-misses onto the sphere for smoother sphere edge without needing to drastically increase the resolution of the particle grid
* Better management of particle spawning to remove motion blur and ensure that it updates frequently enough
* Better calculation of normal / tangent vectors (since they seem to be .... not so great...)
* Update to affect lighting (since right now the particles (and thus the sphere) don't affect the lighting in the scene / don't cast shadows)
* Texture mapping onto the sphere
* Height mapping / displacement onto the sphere (texture lookup)
* Conversion of height map into TSDF for use in ray-sphere ray-sdf intersection calculation
* Addition of atmosphere shader / integration with UE atmosphere system?
* Addition of water shader / integration with UE water system?
* Addition of clouds / integration with UE cloud system?