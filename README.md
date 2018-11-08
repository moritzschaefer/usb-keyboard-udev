# usb-keyboard-udev
arch package to run xmodmap when you plug in your USB keyboard

# references
The code is adapted from: 
http://laurenceoflosangeles.blogspot.com/2015/08/configuring-udev-to-run-script-when-usb.html

There are different ways to write the udev file. Example:
https://superuser.com/questions/249064/udev-rule-to-auto-load-keyboard-layout-when-usb-keyboard-plugged-in

# build

clone the repo, adapt the files (i'm using my own homedirectory), run 

makepkg
and then
pacman -U pkgfile.pkg.tar

# Contribute

I'm new to these packages. If you have suggestions for better locations of the scripts (/usr/bin is not really appropriate for them) and for generalization (i.e. no need to adapt path to home directory) let me know :)
