These rosinstall files are meant to be used in a single `catkin build` workspace. For more info on `catkin build` see [catkin_tools](http://www.github.com/catkin/catkin_tools).


Example usage:

```sh
mkdir ws
cd ws
catkin init
cd src
wstool init
curl https://raw.github.com/jhu-lcsr/rosinstalls/master/$ROSINSTALL_FILE | wstool merge -
catkin build
```
