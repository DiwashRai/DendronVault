---
id: z8fzkjo0zke873q87zu6t71
title: Mouse Sensitivity
desc: ''
updated: 1675099242876
created: 1674508792611
---

### libinput
Use this config file settings in /etc/X11/xorg.conf.d/50-mouse-acceleration.conf
```
Section "InputClass"
	Identifier "My Mouse"
	Driver "libinput"
	MatchIsPointer "yes"
	Option "AccelProfile" "flat"
EndSection
```
