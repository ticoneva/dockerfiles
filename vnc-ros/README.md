[![Docker Pulls](https://img.shields.io/docker/pulls/kaixhin/vnc-ros.svg)](https://hub.docker.com/r/kaixhin/vnc-ros/)
[![Docker Stars](https://img.shields.io/docker/stars/kaixhin/vnc-ros.svg)](https://hub.docker.com/r/kaixhin/vnc-ros/)

vnc-ros
=======
Ubuntu Core 14.04 + LXDE desktop + Firefox browser + TightVNC server + [ROS Jade Desktop Full](http://www.ros.org/). Runs as a daemon by default by using tail.

Build
-----
Include password.txt with the password for TightVNC (by default this is "password"). This must be at least 8 characters and is truncated if longer.

Usage
-----
The default password should be changed. To do so start up a container and then run `docker exec <id> bash -c "echo -e '<password>\n<password>\nn' | vncpasswd"`.

For automatically mapping a VNC port use `docker run -dP kaixhin/vnc-ros` and `docker port <id>` to retrieve the port.
For specifying the port manually use `docker run -d -p <port>:5901 kaixhin/vnc-ros`.
The shell can be entered as usual using `docker run -it kaixhin/vnc-ros bash`.

Citation
--------
If you find this useful in research please consider [citing this work](https://github.com/Kaixhin/dockerfiles/blob/master/CITATION.md).
