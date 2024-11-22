---
title: "Gitconfig"
weight: 1
description: >
  Gitconfig
categories: [devops]
tags: [VersionControl, CICD]
---

gitconfig can either configured globally or per repository 

to configure globally pass `--global` flag

```
git config --global user.name "Rakesh Nagarajan"

git config --global user.email rakesh.core01@gmail.com
```

You can also edit in the file 

~/.gitconfig or  ~/.config/git/config

In these files contains sections, edit the respective sections

Reference
- https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration
- https://git-scm.com/docs/git-config