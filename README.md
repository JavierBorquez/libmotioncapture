[![CI](https://github.com/IMRCLab/libmotioncapture/actions/workflows/CI.yml/badge.svg)](https://github.com/IMRCLab/libmotioncapture/actions/workflows/CI.yml)

# libmotioncapture



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

The original example application is in `examples/main.cpp`. Run it using

```
./motioncapture_example <mocap type> <ip address>

```

To send rigidbody info trough UDP run (Change IP to your mocap as needed.)

 ```
./vicon_sender vicon 192.168.1.39
```

Afterwards run the companion ROS2 node in https://github.com/JavierBorquez/vicon_resend_ws