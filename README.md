CUDA Path Tracer
================

**University of Pennsylvania, CIS 565: GPU Programming and Architecture, Project 3**

* Yash Vardhan
* Tested on: Windows 10 Pro, Intel i5-4200U (4) @ 2.600GHz 4GB, NVIDIA GeForce 840M 2048MB

In this project, I have implemented a CUDA-based path tracer through the use  of GPU. I have implemented some awesome feature like reflection, anti-aliasing, refraction. More to come soon!

![](img/reflection.png)

### Features:
* A shading kernel with BSDF evaluation for:
  * Ideal Diffuse surfaces.
  * Perfectly specular-reflective (mirrored) surfaces (e.g. using `glm::reflect`).
  * Imperfect specular surfaces.
* Path continuation/termination using Stream Compaction from Project 2
* Sort the rays/path segments so that rays/paths interacting with the same material
  are contiguous in memory before shading.
* A toggleable option to cache the first bounce intersections for re-use across all
subsequent iterations. Provide performance benefit analysis across different
max ray depths.
* Work-efficient stream compaction using shared memory across multiple blocks.
* Refraction [PBRT 8.2] with Frensel effects using Schlick's approximation
* Physically-based depth-of-field (by jittering rays within an aperture) [PBRT 6.2.3]
* Stochastic Sampled Antialiasing
* Toggleable Timer

### Results:

# Simple Reflection

![](img/reflection.png)

# Depth of Field

![](img/dof.png)

# Antialiasing

![](img/antialiasing.png)

# Refraction

![](img/refraction.png)