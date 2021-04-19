---
title: A Small CMake Chocolate
date: 2021-04-19T09:57:34.145Z
draft: false
featured: false
external_link: https://georgetattersall.me/project/a-small-cmake-chocolate/
image:
  filename: cmake_logo_slider.png
  focal_point: Smart
  preview_only: false
---
I mentioned in a [ray-casting post I did a bit ago](https://georgetattersall.me/project/ray-casting/) that a fun future project would be to try and make a path tracer in CMake... yes, the build system generator...

A bit of background. I used to hate CMake, all my friends still DO hate CMake... and I can get why. What changed my mind was a trial by fire at IBM. Part of my role there was to completely rewrite their entire build systems (yes, multiple) into a clean unified one... but I didn't know C++ or CMake. It really was very very painful at first, but after 4 months of nothing but linking errors I finally got my first compilation on the new build system! What a way to learn C++, eh? Well during that time I developed a love (Stockholm Syndrome anyone?) for the language, and a respect for how much it can do for you, your code, and your life. I'd happily go into more detail a different day about how great CMake is, but for now, all we need know is it is 100% Turing complete.

With this new information in hand I may direct you to my brief attempt at [the 2019 Advent of Code attempt I made in CMake](https://github.com/Cascades/Advent_Of_Code_2019_CMake/blob/master/3/3-1/CMakeLists.txt) (hence the sugary title). This particular question was something about finding intersections in spirals, and finding the closest one. The input is a list of ups, downs, lefts and rights with a distance for each, forming a path. This task is non-trivial in CMake as the language barely even has array accessing, let alone a maths library that can do anything more than basic operations. Coding useful standalone programs in CMake is so fun BECAUSE of these drawbacks. You have to make everything yourself, and at the end can truly say you MADE the system.

To run the github code just clone it somewhere and run `cmake [path to Advent_Of_Code_2019_CMake/3/3-1]`. You'll see all the output as CMake grinds the numbers.

As I mentioned earlier this is a closest intersection problem... and I know a popular graphics algorithm which relies heavily on such a task! This work proves (to me at least) that intersection testing to possible in CMake, and I can think of way of getting CMake to output colour data to image files, so all in all... I want to make my CMake ray-caster a reality! If only time would allow ;)