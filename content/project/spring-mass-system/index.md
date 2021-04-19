---
title: Spring Mass System
date: 2021-04-19T09:22:09.432Z
draft: false
featured: false
external_link: https://georgetattersall.me/project/spring-mass-system/
image:
  filename: featured
  focal_point: Smart
  preview_only: false
---
<!--StartFragment-->

{{< video library="true" src="cloth.mp4" controls="yes" >}}

<!--EndFragment-->

In a previous post I mentioned [Parent’s fantastic book, Computer Animation: Algorithms and Techniques](https://www.amazon.co.uk/Computer-Animation-Algorithms-Rick-Parent/dp/0124158420). This is once again what I used to develop this project, and I don't know that I could have done it so quickly without the book! Highly recommend to beginners again!

I'll address one thing first. The graphics... I know they aren't the prettiest in this project, but it's not what I wanted to focus on this time around. I have little markers on each mass to show the force they are experiencing, and that's enough for me. The hardest part of the simulation was parameter tuning! It has given me a greater appreciation for why so many papers rave about their methods not needing parameter tuning! For an expert (or the person who wrote the paper) it may very well be obvious which parameters will work, but for me it took a good few days to find some satisfactory ones!

The project itself is a spring-mass model, where I can load in an arbitrary mesh, and each vertex becomes a small mass, with the edges connecting them becoming "springs". These "springs" always apply forces to their connected masses to try and get the springs back to a rest state, while the masses are (almost) always trying to pull them apart! This leads to a constant fighting between the forces, which resolves to this nice simulation of a cloth.

Despite my parameter troubles, I found the project surprisingly satisfying. Surprisingly, because generally I don't like physics programming, something about doing ever more complex integration schemes over time, only to see your beautifully fluid simulations suddenly explode for seemingly no reason frustrates me to no end! I am satisfied that the parameters I chose are stable enough though, and with that fact, I can enjoy the satisfaction of "finishing" the project. I have similar feelings towards most problem solving. It can be painful while figuring it out, but once I've got a system working (especially one I know every inch of) I can revel in the satisfaction of a job well done!

If I had to improve on the project I probably would start with some graphical improvements, possibly I would try and put some of the calculation on the GPU to get larger meshes loaded, or perhaps I would investigate other cloth simulation methods!

I very much hope to get a graphics or engine design post up soon ([Gregory's Game Engine Architecture](https://www.gameenginebook.com/) is another fantastic read! If a little longer...), but for now, thanks for reading!