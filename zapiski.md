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
rospack list  # prikaže seznam paketov
rosrun <package> <node>  # zažene node `node` paketa `package`
```

## Roslaunch
```bash
roslaunch <package> <launchfile.launch> # Zažene launch file `launchfile.launch` v paketu `package`. Uporabno za zaganjanje več node-ov hkrati.
```

## Rosnode
```bash
rosnode list  # prikaže seznam aktivnih vozlišč
rosnode info <node>  # informacije o vozlišču
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

## Rosservice
```bash
rosservice call <service> [argumenti...]  # pokliče storitev `service` s podanimi argumenti
```

## Rosmsg
```bash
rosmsg info <topic> # Pokaže tip sporočila na topic `topic`
```

## Turtlebot
```bash
roslaunch turtlebot_teleop keyboard_teleop.launch # Omogoči kontroliranje Turtlebota s tipkovnico
rviz # Odpre RViz - program za vizualizacijo informacij o robotu
roslaunch turtlebot_rviz_launchers view_robot.launch  # Odpre RViz za Turtlebota, kjer vidimo meritve senzorjev
roslaunch turtlebot_rviz_launchers view_navigation.launch # Odpre RViz za Turtlebota, kjer vidimo navigacijo (G-mapping)
rosrun map_server map_saver -f <file> # Shrani ustvarjeni G-map v datoteko `file`
```
