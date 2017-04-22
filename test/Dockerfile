FROM ubuntu:xenial

MAINTAINER lilee liyingli2018@gmail.com

# setup environment
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update -y && apt-get install -y -q --no-install-recommends locales && locale-gen en_US.UTF-8

ENV LANG en_US.UTF-8
RUN apt-get update -y && apt-get install -y -q --no-install-recommends bash-completion wget vim git iputils-ping terminator supervisor xauth openssh-server sudo

RUN adduser --gecos "ROS User" --home /home/ros --disabled-password ros && \
    usermod -a -G dialout ros && \
echo "ros ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/99_aptget
USER ros

CMD ["bash"]
