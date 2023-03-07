# Ustvarjanje workspace-a

```bash
mkdir ROS
cd ROS
mkdir src
catkin_make
```

```bash
roscore  # (v korenu workspace-a) zažene glavni ROS program

rosrun package node  # zažene node `node` v paketu `package`
rospack list  # prikaže seznam paketov
```
