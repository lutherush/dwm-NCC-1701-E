# My dwm (Dynamic Window Manager) build
###
#
# Author: lutherus
# Last moded:28.03.2020; 16:18
# License: it is a config file. Do what ever you weant but do not blame
# me if it dosnt work
#
#
# Requirements

In order to build dwm you need the Xlib header files.

# Installation

    make

    make install
# Running dwm

Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


# Configuration

The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.
