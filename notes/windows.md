---
id: 5fs80ws2li1d12hstqngu4h
title: Windows
desc: ''
updated: 1678376067388
created: 1678375928402
---

### windows 11 restore old right click menu as default
```shell
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
```

To undo
```shell
reg.exe delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f
```
