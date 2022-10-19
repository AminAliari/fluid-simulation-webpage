---
title: Real-time SPH Fluid Simulation on GPU
description: The hallway smelt of boiled cabbage and old rag mats.
---

This is my final project for the **Animation for Computer Games** course, which was offered by professor [Tiberiu Popa](https://users.encs.concordia.ca/~stpopa/) at [Concordia University.](https://www.concordia.ca/) The topic of my project is implementing *Smooth Particle Hydrodynamics* (SPH) using n-body simulation. I have implemented the governing equations described in [this paper.](http://rlguy.com/sphfluidsim/) Everything is GPU-driven and happens in the compute passes. I have used [The Forge rendering middleware](https://github.com/ConfettiFX/The-Forge) for running my vertex, fragment, and compute shaders on Vulkan and Directx12 APIs. Finally, I thank the author of [this excellent blog post](https://wickedengine.net/2018/05/21/scalabe-gpu-fluid-simulation/) for explaining the GPU implementation details, such as dynamic hash grid and GPU sorting. You can check out the [source code](https://github.com/AminAliari/fluid-simulation) for more details.

## Features
- Spawns particles on a sphere surface. The sphere position and radius can be controlled.
- All simulation parameters, from particle count to equation constants, can be modified through the user interface in runtime.
- The particles are rendered as spheres using instance drawing.
- The camera can move around the scene.
- The simulation can be paused or slowed down while the camera can still be moved.
- The particles collide with different elements of the scene.
- There is a push force at the mouse cursor, and its range and power can be adjusted.

## Videos
{{< youtube lyOMEcvFCTk >}}
</br>
{{< youtube gvYNBDEc8pE >}}
</br>
{{< youtube z8CpxWwnSv8 >}}
</br>
{{< youtube nwySYnyn3e8 >}}
</br>
{{< youtube VVx5kvHPdLc >}}

</br>
</br>

## References
- **[1]** https://en.wikipedia.org/wiki/Smoothed-particle_hydrodynamics
- **[2]** http://rlguy.com/sphfluidsim/
- **[3]** https://github.com/ConfettiFX/The-Forge
- **[4]** https://github.com/GPUOpenLibrariesAndSDKs/GPUParticles11/blob/master/gpuparticles11/src/SortLib.cpp
- **[5]** https://en.wikipedia.org/wiki/Bitonic_sorter
- **[6]** https://wickedengine.net/2018/05/21/scalabe-gpu-fluid-simulation/
<!-- comment -->