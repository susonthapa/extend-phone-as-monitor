#! /bin/sh

# create a new mode
xrandr --newmode "mobile-right" 40.78  960 992 1088 1216  540 541 544 559  -HSync +Vsync

# add the mode to the port
xrandr --addmode HDMI-1 mobile-right

# enable the port and place it right to the embedded Display port (eDP-1)
xrandr --output HDMI-1 --mode mobile-right --right-of eDP-1

# reverse the phone port to the laptop
adb reverse tcp:5900 tcp:5900

# start the x11vnc server
x11vnc -clip 960x540+1920+0 -nocursorshape

