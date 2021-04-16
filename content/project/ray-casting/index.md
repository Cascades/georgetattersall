---
title: Ray-casting
date: 2021-04-16T16:11:12.611Z
draft: false
featured: false
external_link: https://georgetattersall.me/project/ray-casting/
image:
  filename: two-glass-spheres.png
  focal_point: Smart
  preview_only: false
---
<!--StartFragment-->

{{< figure src="ray_image_album/two glass spheres.png" caption="A Cornell Box with two mirrored spheres" >}}

<!--EndFragment-->

For this post I wanted to highlight my adventures into raytracing. There is nothing ground-breaking here, and it seems like a right of passage for all programmer (graphics and not) to create a ray-based rendering algorithm at some point or another.

This ray caster was completely hand made, all the way down to the matrix multiplications. all in C++. It only runs on CPU, but one of many extensions in the future could be to put it on GPU to get quicker convergence, and generally make waiting for renders far less painful.

I also implemented the obj parser that was used to parse the Cornell Box obj, and it's mtl file. The experience was a fun one, and once some fun initial bug (see image below), it worked like a charm!

<!--StartFragment-->

{{< figure src="ray_image_album/artistic.png" caption="Some of the errors were quite pretty!" >}}

<!--EndFragment-->

During the course of the project I mainly worked everything else out myself from what I'd read about in passing before, however there were some moments I turned to [Pharr, Humphreys & Jakob's Physically Based Rendering: From Theory to Implementation](https://www.pbrt.org/) for a deeper dive into topics. I think some natural extensions to this project would be:

* Simply let it run longer to get a prettier image
* Convert some of the functions to CUDA kernels and run it in parallel on the GPU
* Maybe try and use OptiX/RTX style "OnHit", "OnMiss", "OnAny" functions to mimic their APIs
* Try using importance sampling to increase convergence speed
* Develop some BxDF functions
* Millions of other techniques to generally improve performance and quality
* OH! And I really want to write a ray-tracer in CMake... I recon I'd have to be the first... maybe for good reason.

But for now I'll end on a classic Cornell Box

<!--StartFragment-->

{{< figure src="ray_image_album/cornell normal.png" caption="A Traditional Cornell Box" >}}

<!--EndFragment-->