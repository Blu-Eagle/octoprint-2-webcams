# octoprint-2-webcams
how to make OCTOPRINT work with 2 WEBCAMS easily

This process works with 2 webcams but one of them has to be RASPICAM. so you need:

1) RASPICAM (whatever one, (standard, IR-CUT...)
2) Any other USB webcam working with octoprint.

thi idea is very simple, octoprint and MJPEG encoder use few files to configure webcam and those files are:

1) /boot/octopi.txt
2) /root/bin/webcamd
3) /etc/default/webcamd
4) /etc/init.d/webcamd

and in order to reach the second webcam as /webcam2/?action=stream you have to modify also 

5) /etc/haproxy/haproxy.conf

In order to simplify the process I have created the directory tree so that you have just to get a copy the file in the right place.

after that you have done it  you have to run

6) sudo update-rd.d webcamd2 defaults

it might give you an error/alert, but it will have worked.

then reboot

7) sudo reboot

at the reboot you will be able to access the 2 webcams just switching between

/webcam/?action=stream
/webcam2/?action=stream

I am not able to create a plugin for octoprint to simplify the switch between webcams, but if someone does it, please let me know.

ENJOY.
