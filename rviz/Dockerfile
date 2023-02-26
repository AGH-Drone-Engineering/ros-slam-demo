FROM ubuntu:18.04

# Core
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update
RUN apt-get install -y curl gnupg

# GUI
RUN apt-get install -y lxde --no-install-recommends
RUN apt-get install -y xvfb x11vnc
ENV FD_GEOM=1920x1080
ENV FD_SESS=lxde

# ROS
RUN sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
RUN curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | apt-key add -
RUN apt-get update
RUN apt-get install -y ros-melodic-ros-base ros-melodic-rviz
RUN echo source /opt/ros/melodic/setup.bash >> /root/.bashrc

CMD ["x11vnc", "-create", "-forever"]
EXPOSE 5900
