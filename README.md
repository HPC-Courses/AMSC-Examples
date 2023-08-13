# AMSC-Examples

**IMPORTANT NOTE: SInce AY 23-24 I will use the same example repo of my other advanced programming course (advanced Programming for Scientific Computing) also for this course.
The repository is kept only for students of previous years and it is not read only. New students should use the repository in git@github.com:pacs-course/pacs-examples.git**

The Examples for the course on Advanced Methods for Scientific Computing


This repo contains source code and descriptions for the examples and exercises
that will be explained during the AMSC (Advanced Methods for Scientific Computing) course at
Politecnico di Milano.

The repository contains at least one submodule, so to check it out properly you have to type, after having set up an account on [GitHub](https:://www.github.com) and properly set up the ssh keys:

```
git clone --recursive https://github.com/HPC-Courses/AMSC-Examples.gitg
```


The software requires a c++ compiler, i.e. gcc >= 9.0 or clang >= 9.
You may check the version of you compiler with the option -v. Several examples require at least c++14 standard, but better use c++20, since some . Check wether your compile support those standards. You may have a look on [ccpreference.come](https://en.cppreference.com/w/cpp/compiler_support)

You also need to have installed a MPI implementation, for instance [openMPI](https://www.open-mpi.org/) and make sure the compiler supposts [OpenMP](https://www.openmp.org/)

This directory contains some utilities:

**  load_modules
If you use the module system, typing

```
source load_modules
```
or

```
. load_modules.sh
```

load the main modules used in the examples.

**  git submodule **

If you have not used --recursive when cloning this repo and you want to use
the git submodules containing third party software type:

```
./install_git_submodules.sh
```

The file submodule_commands.txt contains some reminder of useful git commands for operating with submodules

```
change_submodules_url.sh 
```
changes the protocol of the submodules to https. You should not need it!

```
change_submodules_url_ssh.sh
```
Change the protocol of the submodules to ssh. You should not need it!

## WHAT DO DO NEXT? ##

- Go to the `Examples/` directory and follow the instructions in the local `README.md` file. 

## What ELSE? ##

  * `Exercises/` Directory with the exercises of the course.
  

