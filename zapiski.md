## Ustvarjanje workspace-a

```bash
mkdir ROS
cd ROS
mkdir src
catkin_make
```

## Uporaba
```bash
roscore  # (v korenu workspace-a) zažene glavni ROS program

rosrun <package> <node>  # zažene node `node` paketa `package`
rospack list  # prikaže seznam paketov
```
## Rostopic
(`roscore` mora teči)
```bash
rostopic list  # prikaže seznam "topicov"
rostopic info <topic>  # prikaže informacije o topicu `topic` (publisherji in subscriberji)
rostopic pub <topic> <message_class> <message>  # objavi sporočilo na topicu `topic`
rostopic echo <topic>  # izpisuje vsa sporočila, ki pridejo na `topic`
rostopic hz <topic>  # izpisuje povprečno frekvenco sporočil, ki pridejo na `topic`
```

## Rosnode
```bash
rosnode list  # prikaže seznam aktivnih vozlišč
rosnode info <node>  # informacije o vozlišču
```

## Roslaunch
```bash
roslaunch <package> <launchfile.launch> # Zažene launch file `launchfile.launch` v paketu `package`. Uporabno za zaganjanje več node-ov hkrati.
```
