# Example project

## Compiling

First, create a directory named `gpgs_build` within this directory:
```
mkdir gpgs_build
cd gpgs_build
```
Then, run cmake using:
```
cmake -DCMAKE_INSTALL_PREFIX=../gpgs_install ../../src/
```
followed by make: `make && make install`.
Now, go to the example directory and create a build folder for that project:
```
cd ..
mkdir example_build
cd example_build
```
Now, run cmake using
```
PATH=$PATH:../gpgs_install/share/ cmake ..
```
followed by make: `make`.
Now everything should have compiled.

## Running

The example program is identical to the one of [`slam_process_ceres`](https://github.com/nilsbore/gpgs_slam#running).

## Problems

Right now, the `eigen_cereal`, `libigl` and `glad` libraries are not properly packaged.
To compile using the same procedure in another directory, you need to make sure that
the paths to these directories are set correctly in the cmake.
This will be fixed eventually.