# HOMEWORK 0: COMPILATION

## Introduction

This assignment gets all the groundwork ready so you can focus on the content in CSE 167. In particular, you will make sure you know how to compile and run modern OpenGL programs with shaders.  Please read the entire assignment (there are multiple pages), including the FAQ on the last tab. 

## Compiling OpenGL Programs

Homeworks 1 and 2 in the class will be using OpenGL programs, including the use of modern programmable vertex and fragment shaders with the OpenGL shading language GLSL.

In principle, OpenGL and related code should be portable across many platforms, and indeed this is its strength. (In both our local classes and previous EdX classes, while there were niggling issues, almost nobody had difficulty getting a working setup, across a wide range of machines, operating systems, and coding frameworks). As such, you may use any computer and platform you choose, but will need some kind of C++ development framework and an installation of OpenGL and GLUT (more on these next).  As a backup, we will try to have at least one of the labs in the CS basement with computers installed with the appropriate software.  

In practice, the above statement is pretty close to true, but you need different installs and tricks to get your machine set up to run the programs for this class properly; this differs on different operating systems. Moreover, the shading language is constantly evolving. Fortunately, we have a detailed FAQ for a variety of different systems.  If you come up with some interesting tricks to get things to work, please post on the discussion boards. As a practical matter, you cannot progress further in the course without being able to compile OpenGL and GLSL programs, and use our automatic feedback systems, so treat this assignment as being of utmost importance.

The skeleton code for the assignments includes the GLM library which is available at http://glm.g-truc.net. This library is header-only, so should be very portable and includes many useful matrix-vector operations, and replacements for many deprecated functions. We have included the zip file and unpacked versions already in the skeletons, and modified include paths appropriately, so you should not need to download anything for GLM.

## Homework 0: Assignment

To make sure you can run programs for the course, please download and compile the homework 0 framework, that can be found from the local CSE 167 website under assignments. Some of you may also wish to browse the lectures in Unit 2 which explain OpenGL and gradually build up the program used for homework 0. (However, Unit 2 is by no means required for homework 0, which just involves setup and compilation.  Also, the current iteration of CSE 167 will slightly update unit 2 to focus on modern OpenGL 3 and up; all skeletons are now written in modern OpenGL; you may want to peruse the slides for OpenGL on the local CSE 167 website).

## Homework 0 Framework

We include complete skeletons for major platforms.  Please access the skeleton code from the local CSE 167 website under assignments.  If you develop on a different platform, you may need to re-create projects and Makefiles from the source code. The next page is a FAQ detailing compilation options.

The Homework 0 program has a textured ground plane with 4 "pillars" and a teapot with lighting that moves.

On Windows, you can run the program by opening the .sln file and pressing F5. On Mac OSX or Linux, you should use the command line to cd to the directory containing the files, type make and ./mytest3.   (Please do not double click on the file using finder in MacOS; that will lead to errors, since the paths would not be set up properly.  Similarly in Windows, please use your C++ development environment for running, by pressing F5 as noted above, rather than double-clicking the executable).  Please also note that the correct way to exit is to hit the ESC key in the program.

Note for this program, the shader directories that contain glsl shaders. These are files that are loaded and compiled by the OpenGL program at runtime and therefore must exist, but need not be part of the Makefile or project.

The mouse can be used to zoom in. Look at the keyboard function in mytest3.cpp to see the keys you can press. The p key will start and stop the animation of the teapot.

Once you have the program running successfully, press i to move the teapot into the correct position for our autograder. Next, press o to output the screenshot to the program's directory. Rename it to "screenshot1.png" so it isn't overwritten by a subsequent screenshot.   Please make sure you do not zoom in or out prior to pressing i or o (if you have earlier played with the mouse, it is best to restart the program and  take the screenshot).   

Next, I want you to change the color of the red highlight on the teapot to yellow (yellow is made by mixing red and green, which are the first two elements of the color vector: the third is blue). This corresponds to a RGBA value of (1,1,0,1). The relevant colors and code are defined in the "display" function of "mytest3.cpp" where it says "add lighting effects." Note that the red highlight is originally somewhat orange with a RGBA value of (1,0.5,0,1). Once you have changed the color of the highlight from red to yellow, recompile, run, and press i then o as before to output a screenshot. Rename this screenshot to "screenshot2.png".

## Future Homework Frameworks

It is a good idea to visit the local CSE 167 website with assignment frameworks, and attempt to compile the later homework frameworks, so that we can catch any compilation issues early.