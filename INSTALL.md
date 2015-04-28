# For OS X only with Homebrew
Please note that [$ means Terminal Prompt]

###Installing GLEW and GLFW3
* brew install --universal glew
* brew install --universal glfw3

###Initial Repo Setup
* $ Fork anton's repo:
[https://github.com/capnramses/antons_opengl_tutorials_book]
* $ Clone your forked repo
[ex:https://github.com/dmsurti/antons_opengl_tutorials_book]
* $ cd `path to your forked clone repo dir`
[ex: cd ~/repos/git/antons_opengl_tutorials_book]
* $ mkdir output ;;; this holds the output of all examples executables

###About Makefiles for OS X

The Makefiles for OS X have been adapted to link to GLEW and GLFW installed via
brew above, while generating all output executables in the `./output`
directory.

The adapated make file is:`Makefile_Brew.osx`.

###Cleaning up *.gcda and *.gcno profile files

Before you run any example, clean up the gcda and gcno files as such, else you
will get the profiling warnings related to mismatched counters and corrupt
tags.

* $ cd `path to your forked clone repo dir`
* $ make -f Makefile_Clean_Profiles.osx

###Running the first_test/main.cpp
* $ cd `path to your forked clone repo dir`
* $ make -f Makefile_Clean_Profiles.osx
* $ make -f `first_test`/Makefile_Brew.osx
* $ ./output/demo

###### will return for example:
Renderer: NVIDIA GeForce GT 650M OpenGL Engine

OpenGL version supported 4.1 NVIDIA-10.2.7 310.41.25f01

###Running all the other examples
* $ cd `path to your forked clone repo dir`
* $ make -f Makefile_Clean_Profiles.osx
* $ make -f `path_to_example`/Makefile_Brew.osx
* $ ./output/`exec_for_example` ;;; to run the example
