# jetson-nano-ros2-yolov8
Docker image for Nvidia Jetson Nano containing ROS2 Iron and Yolov8 (using the GPU)

# What you will find here
A Dockerfile that builds a Docker image for Nvidia Jetson Nano containing 
- ROS2 Iron (with different dependencies that you can tweak in ``ros2_build.sh``)
- Python 3.8
- Yolov8 (doing inferences on the GPU)

# Why ?
Because [dusty-nv/jetson-containers](https://github.com/dusty-nv/jetson-containers) doesn't have a build solution for ROS2 Iron and having Yolov8 running on the GPU.

# Build
```
docker build --platform arm64 -t <your-registry> -f Dockerfile.base .
```

# Acknowledgment
- [dusty-nv/jetson-containers](https://github.com/dusty-nv/jetson-containers) for the ROS2 build script
- [timongentzsch/Jetson_Ubuntu20_Images)](https://github.com/timongentzsch/Jetson_Ubuntu20_Images) for the base image with pytorch