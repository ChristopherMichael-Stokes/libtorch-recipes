# libtorch-recipes
Repository of experiments created with libtorch, with the intention of being reused/modified for future work

# Build dependencies
1. The **libtorch** library.  To obtain, go to https://pytorch.org/ and use the install configurator to generate a download link for your setup.  Under the *package* section choose *LibTorch*, and for *platform* select *C++/Java*, the rest is up to you.
1. Cpp compiler.  You need to ensure you have an up to date compiler supporting at least the cxx11 spec (gnu compiler is my choice). 
1. Build system.  Following guidance from the libtorch docs, all programs will use **CMake** to build, and at least version 3.0 is required.

# How to build and run the code

The first step is to navigate to one of the directories containing a *CMakeLists.txt*, then create a *build/* folder.
Now you need to tell cmake where libtorch is and where to generate build files; my libtorch is located at /usr/share/libtorch, so I use `$ cmake -DCMAKE_PREFIX_PATH=/usr/share/libtorch ./build`.
To run the build process, invoke cmake with `$ cmake --build ./build`.


# datasets

All datasets used are non-propietary, and can be found freely-available online.
For my purposes, I have all my datasets in a '/data/' directory with read only permissions.
