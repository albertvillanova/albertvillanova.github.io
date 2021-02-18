---
title:  "Git: reset commit date"
description: "Reset local commit author/committer dates"
category: til
tags: git
---

To reset the last commit date (both author and committer dates, which are the same within a local repo):
```shell
git commit --amend --no-edit --reset-author
```

To do the same for others than the last commit, rebase instead. To reset last 3 commit dates:
```shell
git rebase -i HEAD~3
```
For all commits, select `e` (`edit`) command instead of default `pick`, and amend them as described above:
```shell
git commit --amend --no-edit --reset-author
git rebase --continue
```

Check that the dates have been properly reset:
```shell
git log --format=fuller
```
