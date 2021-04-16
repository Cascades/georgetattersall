---
title: Mocap IK Engine
date: 2021-04-16T15:25:36.609Z
draft: false
featured: false
external_link: https://georgetattersall.me/project/mocap-ik-engine
links: []
image:
  filename: ik.png
  focal_point: Smart
  preview_only: false
---
<!--StartFragment-->

{{< video library="true" src="IK.mp4" controls="yes" >}}

<!--EndFragment-->

At last, a post about a project! I made this last year after reading [Parent's Computer Animation: Algorithms and Techniques](https://www.amazon.co.uk/Computer-Animation-Algorithms-Rick-Parent/dp/0124158420). I cannot recommend the book enough for someone looking to get a basic understanding of computer animation techniques. It's an easy read and extremely fun!

All of the methods were from the IK and mocap chapters, and were implemented using:

* Eigen - for the relatively high dimensional maths
* Qt - for the experience of using Qt, I had never used it before and learning another technology is always interesting
* OpenGL - used for some very basic rendering

The bulk of the development was making sure to get the Eigen calculations correct. Like most things in development, one little mistake makes all the difference. For me I remember I was creating the initial Jacobian matrix with a classic off by one error. I only found this out after a few days of trying every other more complex solution, including reading up about various types of psuedo-inverses, which was quite an interesting tangent!

Anyway, the results can be seen in the video above. The input is a .bvh file (a mocap format), and at any frame the user can select nodes to be stretched out in a specified direction. The dampening variable is useful for when the target is out of reach as it reduces the effect of the algorithm on the output.

If I were to improve on this I would most likely start with mouse picking, and may include some interpolation between new poses and old ones.