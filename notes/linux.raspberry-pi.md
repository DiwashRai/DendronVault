---
id: j0z7jbe315pr82284cgv3z3
title: Raspberry Pi
desc: ''
updated: 1675166782025
created: 1671098231419
---

### details
**Ethernet:**  
192.168.0.23  
pi/diwashrai  

**Wi-Fi:**  
192.168.0.39  
pi/diwashrai  

### login

Normal verbose  
```shell
ssh pi@192.168.0.23
```

Quick
```shell
ssh pi
ssh pi-wifi
```
uses values from ~/.ssh/config

### Copy ssh keypair to server
`ssh-copy-id pi@192.168.0.23`  
Enter your password. Done  


### NAS start up
```shell
sudo mount /dev/sda /mnt/nas
```

### wifi settings
Might need to select country
```shell
ssh pi
sudo raspi-config
5. Localisation options
WLAN country
```

Or might just need to use rfkill
```shell
rfkill unblock wifi
```