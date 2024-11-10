---
title: "Git"
weight: 2.1
description: >
  Git
categories: [devops]
tags: [VersionControl, CICD]
---

## youtube video link 
## github codebase link 

Version control system
why? --opensource--? 
Local repository/remote repository 
Options in git 
  github
  gittea
  gitlab
  bitbucket
  Azure devops (TFS)

# how to use git effectively, hidden features in git
origin

opensouce/closed -- private repo/
license --?

How to install git?

git - cli

Options in which we can create repo --> local or in repote repo
Platform independent

# to share local copy, without giving remote repo access 
git init --bare /path/to/repo.git 


.gitconfig 
.gitignore --> auto create/ specific to your env 
.gitmodules -->
.gitattributes
.gitkeep


git remote 

# git basics

git --version 


initialize a git repository 

git init 

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
