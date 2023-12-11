# Handle ros distro
ARG ROS_DISTRO=iron-desktop

FROM osrf/ros:${ROS_DISTRO} as ros-ws

ENV DEBIAN_FRONTEND interactive
ENV NVIDIA_VISIBLE_DEVICES all
ENV NVIDIA_DRIVER_CAPABILITIES video,compute,utility

# User provided arguments
ARG HOST_GID=1000
ARG GIT_NAME=""
ARG GIT_EMAIL=""
ARG USE_SIMD=OFF

# Tell docker we want to use bash instead of sh in general
SHELL ["/bin/bash", "-c"]

### Add the user to the current GID of the host to avoid permisson issues in volumes
ENV USER_GROUP=${USER}
USER ${USER}
