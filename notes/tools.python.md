---
id: e7ccw8km6u0an5hyxtkb6zd
title: Python
desc: ''
updated: 1701011313367
created: 1701011158957
---

## Multiple versions of Python on Fedora

### Running specific version of Python

`python` and `python3` are aliases for python3.12 on Fedora 39

```bash
python3.11 --version
python3.12 --version
```

### Getting and using pip for specific version of Python

```bash
python3.11 -m ensurepip --upgrade
python3.11 -m pip install --upgrade pip
python3.11 -m pip install <package>
```