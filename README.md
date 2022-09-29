# Mount FTP
# Mount FTP servers Linux

# Purpose: 
Check if there is an FTP Server in your network and mount it as a filesystem.
If a server is already mounted prompt and Unmount it if it is no longer required.
The mount point is created and destroyed after use 
(to prevent filling the mount directory if the device is not mounted)

Runs on all GNU/Linux distros (install arp-scan) (maybe required. Try without first HHP 20200513)
UBUNTU needs arp-scan (apt install arp-scan)

Authors: Huw Hamer Powell <huw@huwpowell.com>

1) Install arp-scan 'sudo dnf install arp-scan'
2)If you want to use the full functionality of nice dialog boxes install yad . otherwise we default to zenity *not so nice but it works)
3) Change the first three variables according to your configuration. Or maintain a .ini file with the three variables. Can be created by the script if neccessary
4) Run this program at login or from your $HOME  when your network is ready

a mntFTP.desktop file is provided (Copy to $HOME/Desktop)

need to use sudo.. so run the skeleton script mntFTP which will call te script (mntFTP.sh) using sudo... Or from the CLI or Gnome Desktop

# Ensure that you are a valid sudoer and add this line to /etc/sudoers

%wheel	ALL=(ALL)	NOPASSWD: ALL

%sudoers	ALL=(ALL)	NOPASSWD: ALL

Whichever works for you. This will prevent having to enter the sudo password each time it is run

Also, run it on logoff to umount any mounted shares (Will remove the mount point directory).
It does not matter if you don't , Just cleaner if you do :)

----------------------------------------------

Version 1, Cloned from MountNFS
Runs on all GNU/Linux distros (install arp-scan)

Tested on Fedora, UBUNTU, Debian, openSUSE

----------------------------------------------

This program is free software. It comes without any warranty, to
the extent permitted by applicable law. You can redistribute it
and/or modify it under the terms of the "Do What The Fuck You Want To"
Public License, Version 2, December 2004, as published by Sam Hocevar.
See http://sam.zoy.org/wtfpl/COPYING for more details.
or https://en.wikipedia.org/wiki/WTFPL
