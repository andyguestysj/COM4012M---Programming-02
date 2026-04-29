---
marp: true
title: COM4016M - Games Design Lecture 01
theme: beam
paginate: true
header: 'COM4016M - Games Design'
footer: 'Dr Andy Guest, York St John University'

---
<!-- _class: title -->

##

# COM4016M - Games Design

# Dr Andy Guest

---

![Title Image height:600 center](../Thumbs/1.png)


---

## Overview

<div class="columns"><div>

- Administrivia
- Module Content
- Assessment

</div><div>

- Visual Studio Code
- Python Recap
- Pygame
- Object Oriented Programming

</div></div>

---

## Administrivia

- **Lecturer** Dr Andy Guest, a.guest@yorksj.ac.uk, FS114
- **Meetings/Tutorials** [Tutorial Booker](https://outlook.office.com/bookwithme/user/909dd873f8224385958f85e67f6c2923@yorksj.ac.uk/meetingtype/SVRwCe7HMUGxuT6WGxi68g2?anonymous&ismsaljsauthenabled&ep=mlink)
- **Lectures/Labs** - Thursday, 1400-1800, CC106

---

## Module Content

<div class="columns"><div>

- Game development
- Project management
- System analysis
- Problem solving
- Teamwork

</div><div>

![Game Dev](../../Images/modcont.png)

</div></div>

---

## Module Content - Game Development

<div class="columns"><div>

![Game Dev Studio](../../Images/gamedev.png)

</div><div>

- We'll expand your game design / development
- Coding with Python & Pygame
- Content Analysis, Design, Coding
- Managing Game Dev

</div></div>

---

## Project Management

<div class="columns"><div>

- How to manage a project
- Sofware engineering
  - Traditional
  - Agile
- Source Control
- Communication
- Task Tracking
  

</div><div>


![Proj Management/Peak team starting](../../Images/peak.jpg)

</div></div>

---

## Module Content - System Analysis

<div class="columns"><div>

![Analysis/Hitman](../../Images/plan.jpg)

</div><div>

We'll look in to **system analysis** a key part of all software development though we'll focus on games. 

System analysis is the way we examine existing or proposed systems to work out what we need to know to be able to design new software or games. 

</div></div>

---

## Module Content - Problem Solving

<div class="columns"><div>

One of the "fun" things about making games is we constantly have to do things we don't know how to do. Fortunately there are some techniques and tricks that can help - pair programming, rubber duck debugging, etc.

</div><div>

![Problem solving/portal](../../Images/portal.png)

</div></div>

---

## Module Content - Team Work

<div class="columns"><div>

![Problem solving/portal](../../Images/chain.jpg)

</div><div>

Software development is, by and large, a team based activity. Working with other people has its pros and cons. We need to co-ordinate to make sure everything is completed to schedule and works with everyone else's code.

</div></div>

---

## Assessment

![Assessment/Run'n'gun center height:625](../../Images/rungun.jpg)

---

## Assessment

<div class="columns"><div>

- **Full assessment brief will be given soon**
- Group project
- Side-scrolling run'n'gun shooter
- I provide a prototype
- Work together to add new features
- Each take responsibility for a feature

</div><div>

- Expand by adding new features
  - character
  - weapon
  - level
  - enemy
  - boss fight


</div></div>

---

## Visual Studio Code

<div class="columns"><div>

- Time to start using a real IDE
- Visual Studio Code
- Text editor with tools
- Lab session will alk you through getting VSC setup

</div><div>

![Visual Studio Code](../../Images/vsc.png)

</div></div>

---

## Python Recap

<div class="columns"><div>

![Pygame](../../Images/python2.jpeg)

</div><div>

- Quick an dirty reminder of how Python works
- Using VSC to work with Python
- Code
  - variables
  - input & output
  - conditions & branching
  - loops
  - functions

</div></div>

---

##  Pygame

<div class="columns"><div>

- **Pygame** is a game development library for Python
- It handles
  - creating windows
  - drawing graphics
  - processing input
  - etc.

</div><div>

![Pygame](../../Images/pygame.png)

</div></div>

---

## Pygame

<div class="columns"><div>

![Pygame](../../Images/pygame2.png)

</div><div>

We'll look at

- pygame game structure
- the game loop
- processing input
- updating the game
- rendering the graphics
- sound

</div></div>

---

## Object Oriented Programming (OOP)

<div class="columns"><div>

OOP is a way of structuring code around the concept of `objects` which are made of code and data and interact with other objects.

Python can be used to write OOP code. The game prototype is written using objects so we'll fo a gentle introduction to classes and objects in this module.

</div><div>

![Object oriented programming](../../Images/oop.jpg)

</div></div>

---

## Lecture Plan - Subject to change!

<div class="columns"><div>

| Week | Topic |
| :-- | :-- |
| 01 | Introduction  |
| 02 | Pygame, Prototype,<BR/> Assessment Brief |
| 03 | Project Management |
| 04 | Analysis & Design |
| 05 | Problem Solving & Risks |
| 06 | Evaluation |

</div><div>

| Week | Topic |
| :-- | :-- |
| *Easter Break* |
| 07 | Character |
| 08 | Weapons |
| 09 | Level |
| 10 | Enemy |
| 11 | Boss Fight |
| 12 | Finishing Up |

</div></div>

---

<!-- _class: title -->

##

# Visual Studio Code
# (VSC)

---

## VSC

### VSC is

* An Integrated Development Environment (IDE)
  * An application that provides all the tools needed
* A text editor with many free extensions
* Free
* A useful tool for 
  * any programming language
  * web development
  * creating presentations
  * lots of stuff

---

## VSC Installation

### @YSJ

* Is available through AppsAnywhere
* Needs to install Python first (let it)

### @Home

* Download the correct version from [https://code.visualstudio.com/](https://code.visualstudio.com/)

---

## VSC Basics 1

<div class="columns"><div>

VSC should run after you install it. It should find the Python installation automatically. You may need to configure it for other uses.

VSC has the traditional menu across the top, an icon bar down the left hand side and a main viewing area.

The image to the right shows my VSC when I was putting together this lecture.

</div><div>

![Visual Studio Code center](../../Images/vsc2.png)

</div></div>

---

## VSC Basics 2

There are different ways to do most things in VSC - menu options, key presses, the icon bar/left hand window and pressing `Ctrl` + `Shift` + `P` together to bring up a command prompt at the top of the window.

When I explain how to do something I'll explain it my way, which varies from task to task. Remember you can check out the other ways if you find them better.

---

## VSC Layout

|||
|--|--|
| ![VSC Layout center height:600](../../Images/vsclayout.png) | **Coloured Areas** <BR/><span style="color:green;">Menu Bar</span> <BR/> * Typical menu functions <BR/><span style="color:red;">Icon Bar</span> <BR/> * Changes the explorer window <BR/> <span style="color:#AA336A;">Explorer Window</span> <BR/> * Browser for selected feature <BR/><span style="color:blue;">Main window</span> <BR/> * Area for editor, preview, terminal windows, etc. |

---

## VSC Extensions

<div class="columns"><div>

![VSC Extensions installation height:550 center](../../Images/extensions.png)

</div><div>

There are many free extensions available for VSC such as 

* coding in different programming languages, real languages too.
* text editing
* generation of html, pdfs, etc
* AI tools
* many more

You can use the search bar to find specific extensions and the filter to find recommendations, popular, etc.

</div></div>

---

## VSC Module Setup - Extensions

For this module we will install some extensions to make working with Python better.

* Click the `Extensions` icon in the icon bar.
* Click the search bar in the explorer window.
* Type each of these in to the search bar and click `Install`
  * Python Extension Pack
  * Git Extension Pack
* These aren't essential but are nice to have
  * indent-rainbow
  
---

## VSC Module Setup - GitHub 1

You can remotely store your VSC settings so when you use a different computer you just have to sign in to that account and VSC should grab all the extensions you need and fix any other settings.

I'm going to recommend you create a GitHub account, if you don't already have one. Go to [github.com](github.com) and `Sign up` for an account. (Use a sensible name!). Make sure you remember the name!!

In VSC at the bottom of the icon bar is an icon of a person in a circle. Click it and select `Sign in to sync settings`. Sign in using the GitHub account you just created.

When you use a different computer you can sign in the same way. Without creating a new github account of course.

---

## VSC Module Setup - GitHub 2

To be able to use GitHub easily we need to tell you computer a couple of things about you - namely your name and email address for when you upload code changes.

In VSC, from the Menu select `Terminal`, `New Terminal` and you should get a terminal window appearing at the bottom of your main window.

Select the terminal and type the following commands, switching out my name and email address for yours.

```console
git config --global user.name "Andy Guest"
git config --global user.email "a.guest@yorksj.ac.uk"
```

These are computer settings and don't always follow you with the VSC account so you may need to type these in again when you use a new machine.

---

## VSC Hello World Python 1

In VSC select `Open Folder` from the menu, the start screen or from the explorer window after selecting `Explorer` on the icon bar. If you can's see it then close any files you have open in VSC first.

Next browser to the folder you want to store your python work in. Right click in the folder window, select `New > Folder` and enter the folder name `helloworld`. Press enter and then click the `Select folder` button.

You should now be back in VSC with a `Welcome` window in the main area, the `Explorer` browser on the right with `HELLOWORLD` at the top of it.

---

## VSC Hello World Python 2

![Empty python project for hello world center height:550](../../Images/helloworld2.png)

---

## VSC Hello World Python 3

Create a new file in the project and call it `helloworld.py`. You can do this from the `Welcome` window, the start menu, etc. You'll be prompted where to put it. Put it in the folder you created, which should be the default you are offered.

In `helloworld.py` enter the following code

```python
print("Hello World!")
```

Save the file and run the code by one of..
* using the play button at the top left of the `helloworld.py` window. (You might need to use the drop down and select the first option once to make the button work)
* Right click in the `helloworld.py` window and select `Run Python > Run Python File in terminal`
* typing `python ./helloworld.py` in a terminal
* another way :-)

---

## VSC Setup Sorted

That's pretty much everything setup for you to start working in Python. We'll cover anything that comes up when it comes up.

**Also**

* Python Refresher
* Git Refresher
* OOP Refresher

---

## Next Week

<div class="columns"><div>

* **Pygame**
  * What is it?
  * How do I get it?
  * How do I use it?
  * How does it work?

</div><div>

* **Game Prototype**
  * Git Repository
  * How does it work?
  * What do we do with it?
* **Assessment Briefing**

</div></div>

