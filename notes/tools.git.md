---
id: 04uwy15ipgua4lzrmnrr5vg
title: Git
desc: ''
updated: 1676229978119
created: 1664675034543
---

## General commands

### Create a new branch and push to remote repository
```shell
git checkout -b <branch>
# Edit files, add and commit. Then push with the -u (short for --set-upstream) option
git push -u origin <branch>
```

### Revert commit
To commit the previous commit
```shell
# get commit hash of desired commit. In this case the previous one
git log -1 
# git revert with correct hash
git revert 11d172998d218c5e25e949fc82a3df3b41a241bd
```

### Removing untracked files
```shell
# show what files would be deleted
git clean -n
# show what directories would be deleted
git clean -nd
# delete untracked files
git clean -f
# delete untracked files in specific folder
git clean -f path/to/folder
# delete untracked files AND folders
git clean -fd
# delete ignored files
git clean -fx
```

### Git reset
Command to unstage changes
```shell
# commit parameter is optional. By Default it points to head.
git reset <commit> -- <path>
# unstage all changes and discard them.
git reset - -hard <commit>
```

### Discard unstaged changes on Git
To discard unstaged changes, use the `git checkout` command.  
This means to undo any local changed that a checked in file may have  
```shell
# to unstage on file at a time
git restore path/to/file/to/revert
# to unstage everything in one go
git restore .
```

### Git add
```shell
# stage all changes
git add -A
# stages new files and modifications, **without deletions**
git add .
# stages modifications and deletions, **without new files**
git add -u
```

### Edit git config file
```shell
git config --config --edit
```

### Reading last commit
```shell
# show last commit only
git log -1
# show head commit
git show
```

### Git commit with specific date
```shell
git commit --date 2022-01-20
```

## Creating Git repo locally
- Run `git init` in the project directory
- Create .gitignore fiel

## Pushing Existing local git repo to GitHub
- Make sure you have a local git repo initialised
- Create empty git repo on GitHub
- Open a terminal and run:
  - `git remote add origin <github repo link>`
  - `git push -u origin main`
    - `-u --set-upstream`
