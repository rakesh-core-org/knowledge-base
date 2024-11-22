---
title: "Git"
weight: 1
description: >
  Git
categories: [devops]
tags: [VersionControl, CICD]
---




Git is designed by linus Tovalds for managing linux kernel development.
Platform independent, works with (linux,mac,windows)

### Popular Git-based platforms
  - github
  - gittea
  - gitlab
  - bitbucket
  - Azure devops (TFS)

[Reference github organization](https://github.com/rakesh-core-org/)

why? --opensource--? 
Local repository/remote repository 
Options in git 

### Access git
  - git cli
  - git platforms
  - git GUI

### Install git client

Inorder to access git, we need to install git client in our local machine(where we are accessing git)
By default all major distributions ships with git, better update the package

### how to use git effectively, hidden features in git
origin

opensouce/closed -- private repo/
license --?

Options in which we can create repo --> local or in repote repo
Platform independent

### to share local copy, without giving remote repo access 



### Hidden files and folders usage
.gitconfig 
.gitignore --> auto create/ specific to your env 
.gitmodules -->
.gitattributes
.gitkeep
.git

git remote 

### git basics

git --version 


### Initialize a git repository 

git init 

git init --bare /path/to/repo.git 

this creates a .git directory --> local to your env
- hooks 
- info
- objects
- config
- description
- HEAD

commit_ID

staging area / 

`git log`

Add blank commit, to test CI 
`git commit -m "blank commit" --allow-empty`

commit at a specific date 
`git commit -m "fix bug" --date 2024-12-12`

Merge two local commits before pushing to remote 
`git commit --ammend "this is ammend message"`


Temproarily mark a file as untracked

```
git update-index --assume-unchanged filename.sh
git update-index --no-assume-unchanged filename.sh 
```

git reset

git rebase 

git cherry-pick 
