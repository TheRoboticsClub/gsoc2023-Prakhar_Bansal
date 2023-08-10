---
title: "Coding Period Week 7"
categories:
  - Blog
permalink: /Coding-period-week7/
toc_label: Table of Content
toc: true
sidebar:
  nav: "docs"
---

Over the past week, I've been working on a project to put the entire robotics academy's software into a single .exe file. It turned out to be quite a learning experience, as there were several challenges I had to tackle along the way.

I used a technology called Electron to help with this task, but there was a tricky part. The software relies on something called Django for its backend, and making everything fit together was a bit like solving a puzzle. One big issue I encountered was that when trying to bundle everything up, there were some special kinds of links that didn't work as expected. These links are like shortcuts that help different parts of the software find each other, but they got confused because they couldn't find the right version of a computer language called Python.

After some digging, I found out that the solution involved creating a special kind of environment for the software to work in. This environment needed to be set up in a certain way to make sure everything would be packaged correctly. It turns out that this environment also has a version of Python inside it, but we had to be careful about which parts of it we included.

Eventually, I managed to create the .exe file, which is the type of file that you can run like a regular program. But there was another challenge waiting. Even though the file worked, the software inside couldn't connect properly to its backend – the part that handles data and calculations. This is going to be my focus for the coming week. I'm planning to use something called Docker to help make that connection work smoothly.

To sum it all up, this past week has been quite a journey. From dealing with technical details of how software pieces fit together, to figuring out how to make them cooperate inside a single file – it's been an adventure of learning and problem-solving.

## Work Done

- Packed the Robotics-academy application into a .exe file

## Learnings

- When bundling an application, symbolic links, often referred to as symlinks, present both opportunities and challenges. These links act as references to other files or directories, enabling efficient sharing and organization of resources within a file system. However, during the bundling process, symlinks can introduce complexities.

When packaging an application, especially one with multiple components or dependencies, the presence of symlinks can impact how the bundled content is organized and accessed. Depending on the technology used for bundling, such as Electron in your case, symlinks might behave differently. They could potentially break if not handled correctly, leading to issues with locating the linked resources within the bundled application.

Symlinks can also create complications when attempting to bundle an application across different environments or operating systems. Since symlinks reference file paths, these references might not hold up if the application is moved to a different location or system where the original paths no longer exist. This situation can necessitate adjustments to ensure that the symlinks remain valid and functional within the bundled application.

In this scenario, while bundling a Django backend with Electron, it's important to consider the impact of symlinks on the virtual environment and the paths to Python interpreters. The decision to create the virtual environment without including pip was a strategic move to streamline bundling, highlighting the need to carefully manage the interactions of symlinks within this environment.

## Plan for Next week

- Initialise the strucutre for the electron and proceed with the build
- Figuring out a way to run the docker image from within the electron
