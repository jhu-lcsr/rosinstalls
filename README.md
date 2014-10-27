LCSR rosinstalls
================

A collection of rosinstall files for quickly downloading LCSR ROS packages.

## Usage

To create a new workspace:

```bash
mkdir -p ~/my_ws/src
cd ~/my_ws
catkin init
cd ~/my_ws/src
wstool init
```

To load any rosinstall files from this repository into your workspace (replace `PATH/TO/FILE` with the appropriate file relative to the root of this repository):

```bash
curl https://raw.github.com/jhu-lcsr/rosinstalls/master/PATH/TO/FILE.rosinstall | wstool merge -
```

Once creating this workspace, you can build it in the following manner
(this will create a pair of chained Catkin subspaces):

```sh
cd ~/my_ws/src
unset CMAKE_PREFIX_PATH
source /opt/ros/$ROS_DISTRO/setup.sh
catkin build
```
