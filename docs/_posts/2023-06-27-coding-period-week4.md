---
title: "Coding Period Week 4"
categories:
  - Blog
permalink: /Coding-period-week4/
toc_label: Table of Content
toc: true
sidebar:
  nav: "docs"
---

In our recent endeavors, we dedicated our efforts to address the essential packages and dependencies essential for seamless operation of the Django server. However upon setting up our django server we encountered dependency issues which required the installation of **pylint**  and **django-corse-headers**

[!Errors](../assets/images/Codingweek4img1.png)
\
[!Errors](../assets/images/Codingweek4img2.png)

## Work Done

* The server worked when the above dependencies were installed
* Updated the *InstructionsForDevelopers.md* in docs

## Learnings

* Tried updating the missing dependencies in *requirements.txt* But it resulted in multiple package conflicts which when tried to fix compounded further

* MySQL client needs to be setup before installing the *mysqlclient* python package 

## Issues Raised
[Issue](https://github.com/JdeRobot/RoboticsAcademy/issues/2167)

## PR's Created
[PR](https://github.com/JdeRobot/RoboticsAcademy/pull/2168)