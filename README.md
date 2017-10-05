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

sudo update-rd.d webcamd2 defaults

