---
layout: default
title: Documentation
nav_order: 5
description: "Installation and usage."
permalink: /documentation.html
---

# Documentation

```
ATTENTION: This page is not complete for the latest version. 
It will be completed as soon as possible.
```

## Overview

Aestimo Self-consistent Schrödinger-Poisson Solver (simply aestimo) is a simple 1-dimensional (1-D) simulator for semiconductor heterostructures. Aestimo is started as a hobby at the beginning of 2012, and become a usable tool which can be used as a co-tool in an educational and scientific work.

Hope that it also works for you. Please do not hesitate to contact us in case of any bugs found.

The documentation material on this page is copyrighted. Reuse of the material on this wiki is permitted under GNU Free Documentation License 1.3.

### Current features

* Material and alloys: GaAs, AlAs , InAs, InP, AlP, GaP, AlGaAs, InGaAs, InGaP and AlInP,
* Band structure for gamma electrons and heavy, light and split-off holes,
* Effective-mass method for electrons and 3×3 k.p method for holes,
* Carrier concentrations for gamma electrons and heavy, light and split-off holes,
* Electric field distribution,
* Electron wavefunctions,
* Non-parabolicity,
* External electric field,
* Strain for valance band calculations,

### Getting Started

See the see the examples subdirectory of the distribution. Also, detailed information can be found in “Using the Code” part of this document. For developers and people interested in latest development issues, there is an aestimo-devel mailing list. Subscription to the aestimo-devel mailing list is highly recommended for users for further support.

### License

The software is released under the GPL license, which means that everyone is free to download, use, and modify the code without charge.

## Download and Installation

The latest version of the program is available in zipped form from the website: https://bitbucket.org/sblisesivdin/aestimo/.

### Prerequisites

You will need to have a recent version of Python installed on your computer. For this, please refer to Python Website, where binary packages for most platforms can be found. Additionally, you need libraries called numpy and pylab. Both can be obtained from the Scipy Website.

For Macintosh, Python is preinstalled and related libraries can be found at Pythonmac Directory.

### Running the Code

Most of the code is written in Python, and thus is platform independent. After extracting the aestimo_x.y.zip file to a folder, user may point the files that are written below in the related folder. Here x.y is the version number.

```
main.py - The file that you need to run. 
config.py - A simple configuration file. You must enter the input filename into this configuration file. database.py - A database for materials properties. 
aestimo.py - Main program for conduction band calculations and gamma valley electrons. Its code is simple to understand. 
aestimo_numpy.py - Main program which uses the Numpy library. Use this one for your conduction band calculations and gamma valley electrons. 
aestimo_numpy_h.py - Calculator for valence band calculations and holes. 
VBHM.py - A class file for 3x3 k.p method. 
sample-X.py - Some samples files (X) are included in the package with prefix "sample-". 
main_iterating.py - A script for simulating a design several times while varying a parameter over a range of values. 
README - A readme file as you noticed. 
README_OUTPUTS - A readme about the structure of output files. 
COPYING - License of the software. 
AUTHORS - List of the committers. 
/outputs - Output folder /outputs-numpy - Output folder for numpy version.
```

First of all, user must prepare or use an input file. This file must specified in config.py file. There are other options in config.py file like necessary output files and on/off options for result viewer and in-run messages. After specifiying an input file in config.py, user can run the aestimo easily with executing the command

```
./aestimo.py
```

or

```
./aestimo_numpy.py
```

for conduction band calculations. For valence band calculations, aestimo uses a 3×3 k.p model which includes strain. After editing config.py for input file, execute the command

```
./aestimo_numpy_eh.py
```

For simulating a design several times while varying a parameter over a range of values, edit the main_iterating.py file for your needs, and then execute it as

```
./main_iterating.py
```

If the output file options are true in config.py file, results can be found in the outputs folder as:

```
sigma.dat - Areal charge density 
efield.dat - Electric field 
potn.dat - Electric potential 
states.dat - Values of states in the related quantum region 
firststate.dat - Probability distribution of first quantum state
```

## Aestimo Command Reference

### Format of Input File

aestimo input files are simple python files. Each line is a statement or a comment. Statements are shown as python variables. These variable are equalized to parameters. Right hand side of equal sign is the parameter part. Therefore, the statement/parameter pairs have the format as

```
statement = parameter
```

or

```
statement = [[param11, param12], [param21, param22]]
```

In addition to statement/parameter lines, lines can be also blank and comment lines. Comment lines are shown

```
# Comment line
```
Comments can also be added at the end of statement/parameter lines as

```
statement = parameter # Comment is at the end
```

In addition to these, there is python related lines. These lines are the first two lines of the file.

```
#!/usr/bin/env python 
# -*- coding: utf-8 -*-
```

First one is the line which shows the place of python executable in a UNIX-like system. Second line is about coding. These lines can stay as they. Because of input files are just python files, and the statements are python variables, statements in aestimo are sequence insensitive. Parameters may be one of four standard python types: float, integer, bool, string. All the parameter specification has the same format as

```
parameter_name = [number|integer|bool|string]
```

Statements and string parameters are mostly case sensitive.

### Statement Description Format
Will be here.

### General Settings
Will be here.

### Regional Settings
Will be here.

## Todo/Wish List

Since this is a small project, there are many things to do. If you can not do any desired calculation with aestimo please look at this todo first. Required features may not be implemented in aestimo for now. And troubleshooting below is also a pathfinder for your calculations.
* Implement quantum region(s),
* Current characteristics with a simple mobility model,
* Schottky contacts,
* More complex boundary conditions,
* C/V characteristics,
* Support for piezoelectric and pyroelectric charges (wurtzite structures),
* Many input files can be inserted to config.py file like a queue.

## Troubleshooting

* *Program is not converging!*: Aestimo is not a mature tool. Therefore it is selective in calculations. Convergence problem can be raised from mainly two reasons: Gridfactor is not small enough and structure is highly doped. Please use smaller gridfactor (<1nm) and low doping concentrations (<1e17 cm^-3).

## Copyright information

Aestimo 1D Schrodinger-Poisson Solver
Version v.0.6 - v.1.2
Copyright (C) 2013-2017 Sefer Bora Lisesivdin and Aestimo group

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. http://www.gnu.org/copyleft/gpl.txt .

For the list of contributors, see [AUTHORS](AUTHORS.md).
