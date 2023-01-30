---
id: j0z7jbe315pr82284cgv3z3
title: Raspberry Pi
desc: ''
updated: 1675099199029
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
`ssh pi@192.168.0.23`

Quick
`ssh pi` - uses values from ~/.ssh/config
`ssh pi-wifi`

### Copy ssh keypair to server
`ssh-copy-id pi@192.168.0.23`
Enter your password. Done


### NAS start up
```
sudo mount /dev/sda /mnt/nas
```

### wifi settings
Might need to select country
```
ssh pi
sudo raspi-config
5. Localisation options
WLAN country
```

Or might just need to use rfkill
```
rfkill unblock wifi
```