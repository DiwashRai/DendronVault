
### libinput
Use this config file settings in /etc/X11/xorg.conf.d/50-mouse-acceleration.conf
```ini
Section "InputClass"
	Identifier "My Mouse"
	Driver "libinput"
	MatchIsPointer "yes"
	Option "AccelProfile" "flat"
EndSection
```
