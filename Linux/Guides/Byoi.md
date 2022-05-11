## BYOI ArcoLinuxB Plasma

1. git clone https://github.com/arcolinuxb/arco-plasma
2. change packages.x86_64 – we just change some of the
   applications arbitrarily.
3. run script 30 if you build the iso for the first time.
4. run script 40 if you build the iso for the second time
   (more conservative for your bandwidth usage).

* Never run the building script with sudo just `./30-build-the-iso...`

* Use the /personal folder to add configs, backgrounds,
  packages, settings, etc to the ISO.
* Use the alias `personal` to copy/paste them over.

* Run this script always in bash (standard).
* ***NOT IN ZSH!!***

* If you want to autologin.
- Change or edit `/etc/lightdm/lightdm.conf` to:
```config
    autologin-session=your desktop.
```
- or use our ArcoLinux Tweak Tool.

* You can find the name of your desktop in `/usr/share/xsessions`.

* You can always set your num lock key on with "`numlockx on`"
  in the terminal or in your .bashrc.
