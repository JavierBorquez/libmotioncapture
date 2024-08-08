[![CI](https://github.com/IMRCLab/libmotioncapture/actions/workflows/CI.yml/badge.svg)](https://github.com/IMRCLab/libmotioncapture/actions/workflows/CI.yml)

# libmotioncapture

```

For C++, follow the instructions below.

This is a fork of https://github.com/IMRCLab/libmotioncapture with the following changes:

- UDP tunnel to ROS2 odometry publisher
- Only tested with Vicon mocap so far


## Prerequisites

```
sudo apt install libboost-system-dev libboost-thread-dev libeigen3-dev ninja-build
```

## C++

```
git submodule init
git submodule update
mkdir build
cd build
cmake ..
make
```

An example application is in `examples/main.cpp`. Run it using

```
./motioncapture_example <mocap type> <ip address>
```

