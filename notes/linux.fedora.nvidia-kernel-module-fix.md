---
id: 56lg0varlaxfojim4yyv3af
title: Nvidia Kernel Module Fix
desc: ''
updated: 1670957596050
created: 1670094259336
---

### commands to run to fix
```
sudo dnf remove xorg-x11-drv-nvidia-\* akmod-nvidia
sudo dnf install akmod-nvidia
sudo dnf reinstall kernel\*
reboot
```

### secure boot
Even with the above fix, the module not might load. Disable secure boot and it should work.