## Weston

If Weston fails to start double check /etc/xdg/weston/weston.ini and verify that the output name and screen resolution matches the configured U-Boot environment, for example on Renesas Porter board rev 1.0 with screen resolution 1024x768:

```
[core]
shell=desktop-shell.so
backend=drm-backend.so

[shell]
locking=true
# Uncomment below to hide panel
#panel-location=none

[output]
name=HDMI-A-1
mode=1024x768
#mode=1920x1080
#mode=173.00  1920 2048 2248 2576  1080 1083 1088 1120 -hsync +vsync
```

# Debugging

It is possible to debug AGL images on Renesas Porter board using USB to Mini-B USB cable. Plug the USB connector of the cable to your computer and use your favorite tool for serial communication. For example on Ubuntu and other Linux distributions you may use screen:

```
sudo screen /dev/ttyUSB0 38400
```
