---
id: 04uwy15ipgua4lzrmnrr5vg
title: Git
desc: ''
updated: 1664675589329
created: 1664675034543
---

## General commands

### Git reset
Command to unstage changes
- `git reset <commit> -- <path>` commit parameter is optional. By Default it points to head.
- `git reset - -hard <commit>` unstages all changes and discards them.

### Remove unstaged changes on Git
To remove unstaged changes, use the `git checkout` command.
- `git checkout -- <path>` to unstage on file at a time
- `git checkout .` to unstage everything in one go

### Git add
- `git add -A` stages **all changes**
- `git add .` stages new files and modifications, **without deletions**
- `git add -u` stages modifications and deletions, **without new files**

### Edit git config file
- `git config --config --edit`

### Reading last commit
- `git log -1`
  - shows last commit only
- `git show`
  - shows head commit by default

### Git commit with specific date
- `git commit --date 2022-01-20`

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
