---
id: 56lg0varlaxfojim4yyv3af
title: Nvidia Kernel Module Fix
desc: ''
updated: 1688209317759
created: 1670094259336
---

### commands to run to fix
```shell
sudo dnf remove xorg-x11-drv-nvidia-\* akmod-nvidia
sudo dnf install akmod-nvidia
sudo dnf reinstall kernel\*
```

Check the module is built and loaded
history last should show something like this
```shell
dnf history list last

ID     | Command line                                                                                            | Date and time    | Action(s)      | Altered
--------------------------------------------------------------------------------------------------------------------------------------------------------------
    64 | -y install --disablerepo=* /tmp/akmods.iy9iafLS/results/kmod-nvidia-6.3.8-200.fc38.x86_64-535.54.03-1.f | 2023-07-01 11:58 | Install        |    1 EE

reboot
```

### secure boot
Even with the above fix, the module not might load. Disable secure boot and it should work.