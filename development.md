---
layout: default
title: Development
nav_order: 7
description: "Development pages"
permalink: /
---

# Developer's Guide

## Introduction

Welcome developers. Before beginning technical subjects, it will be better to talk about Aestimo, its aim, its place among the other simulators.

Aestimo is aimed to be both educational and research tool. For educational purposes, it must be easy to understand. For research, it must have some point of computational correctness and sensitivity.

If you are looking for a motto for project (we do not have any) or a sentence that explain aestimo, it will be the “The less you have, the more creative you are”

Therefore, we must try the best with minimum code addition. With python, it is impossible to do anything with big add-ons like numpy, pylab,…etc… but this is something else. The aestimo code itself must be minimalist and easy to read. For example: We can use input files in two ways:

* With writing a huge parser, which parses input file line by line and make it usable
* Or make input file as python file, so you can only import to use.

So, our choice must be the latter one.

Not everybody can code in object-oriented way, so start with the known way :) We can discuss it in maillist. Use comments in code as many as possible. Learn to use git. Push your changes and make us review it. Before begin

Before beginning to code, there some references that you may interested in:

* Paul Harrison, Quantum Wells Wires and Dots book. Our code is mostly built on Harrison’s code. Book’s all code is listed at here and the code itself can be found at here. It may be better to look at updates of the code.
* A computational physics book which you can find on the internet: Morten Hjorth-Jensen, “Computational Physics”, Univ. Oslo, 2007. There is also a 2011 dated lecture notes of it. 
* A very good source of numerical methods with python codes: Jaan Kiusalaas, “Numerical Methods in Engineering with Python”, Cambridge, 2010.

Some thesis and dissertations about the subject:
* Jonathan Edward Moussa, “The Schrodinger-Poisson Self consistency in Layered Quantum Semiconductor Structures” M.Sc., Worchester Polytechnic Inst.,2003.
* Nuno Sucena Almeida, “Development of a Multi-physics Simulation Framework for Semiconductor Materials and Devices” M.Sc., Boston Univ., 2005.
* Jeffery Wayne Allen, “A Simulation Tool Suite for the Modelling and Optimization of Multiple Quantum Well Structures” The University of Texas at Arlington, 2005.

You can ask to Dr. Lisesivdin if you have problems with reaching to these references.
## Todo / Tasks

*Legend: 1:High priority, 2: Normal priority, 3: Low priority*

* Implement quantum region(s): (Priority:2) (Assigned to na) (Deadline: na)
* Current characteristics with a simple mobility model: (Priority:3) (Assigned to na) (Deadline: na)
* Schottky contacts: (Priority:2) (Assigned to na) (Deadline: na)
* More complex boundary conditions: (Priority:2) (Assigned to na) (Deadline: na)
* C/V characteristics: (Priority:3) (Assigned to na) (Deadline: na)
* Support for piezoelectric and pyroelectric charges (for wurtzite structures): (Priority:1) (Assigned to na) (Deadline: na)
* Many input files can be inserted to config.py file like a queue: (Priority:3) (Assigned to na) (Deadline: na)
* Preliminary User documentation: (Priority:2) (Assigned to Dr. Koziol) (Deadline: December 2013)
* Implementing a better band structure calculation method instead of using band offsets (Priority:1) (Assigned to na) (Deadline: na)

## Recently Completed Tasks

* Clean-up code: (Priority:1) (Assigned to Dr. Steed) (Deadline: April 23th, 2013)
* External electric field: (Priority:1) (Assigned to Dr. Steed) (Deadline: April 23th, 2013)
* Implement holes: (Priority:1) (Assigned to Hamza Hebal) (Deadline: version 0.8)
* Non-parabolicity: (Priority:1) (Assigned to Dr. Steed) (Deadline: version 0.8)
* More materials: (Priority:1) (Assigned to Dr. Lisesivdin (Thanks to Dr. Beyza Sarikavak-Lisesivdin for material parameters) (Deadline: version 0.8)

## Release Plan

Before become a stable release, after completing every 1-3 tasks, new version can be released like 0.7, 0.8… With a agreed discussion on that we have a preliminary stable release, we will open the code to the public, and we can proceed with a new and logical release plan like:

```
First freeze time : Every 1 March 
First release time : Every 31 March 
Second freeze time : Every 1 September 
Second release time : Every 30 September
```

Freeze times are the development freeze times. One month before every release, we must freeze the development as its current state. In that month, reviews of codes, testing will be completed. If the total development is not large or negligible, it will be a minor release. Assignments

For a small project with a small group, it may be better use assignments. Please inform when you interested in one or more than one of the tasks written above. So, we can prevent to work more than one person working on same task. Assignments will have deadlines.
