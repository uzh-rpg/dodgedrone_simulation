# Prerequisites


## Kinetic
```
sudo apt-get install ros-noetic-web-video-server ros-noetic-rosbridge-server
```

# Install on demopc (roscore/websocket)
Download and run apache web server. Rename HTML info file.
```
sudo apt-get install apache2
sudo service apache2 restart
```

Rename file and link web interface:
```
roscd dodge_web_interface
pwd=`pwd`
cd /var/www/
sudo mv html html.backup
sudo ln -s $pwd/html/
```

# Try it out
On the computer:
```
roslaunch dodge_web_interface servers.launch quad_name:=your_quad
```