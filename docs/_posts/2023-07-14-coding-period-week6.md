---
title: "Coding Period Week 6"
categories:
  - Blog
permalink: /Coding-period-week6/
toc_label: Table of Content
toc: true
sidebar:
  nav: "docs"
---

This week after intializing and successfully serving the react frontend inside an electron instance we wanted to run the django server concurrently with the electron instance, To do so we decided to use commands to start the django server in a bash terminal using *spawn* from electron which spawns a child process which is carried out using the followind command :

```js
createDjangoServer = () => {
  const activateCommand = source ${rootPath}/env/bin/activate && ;
  const command = python3 ${rootPath}/manage.py runserver;

  const fullCommand = activateCommand + command;
  const fullArgs = ['-c', fullCommand];

  childProcess = spawn('bash', fullArgs);
}
```

However even after quitting the electron application the child process still continued to run therefore we had to add a function that kills the child process when the application window is closed

```js
const killDjangoServer = () => {
  if (childProcess) {
    childProcess.kill();
  }
};
```

Hence now the user does not have to manually start the django server to use the Robotics Academy Exercises. They can directly access the application by using one command in the console i.e

```console
yarn start
```

## Work Done
* Updated Index.js to run the Django server when the application is initialized
* Decreased the manual commands the user had to perform previously to use Robotics Academy 

## Issue
[https://github.com/JdeRobot/RoboticsAcademy/issues/2172](https://github.com/JdeRobot/RoboticsAcademy/issues/2172)

## PR's created
 [https://github.com/JdeRobot/RoboticsAcademy/pull/2173](https://github.com/JdeRobot/RoboticsAcademy/pull/2173)