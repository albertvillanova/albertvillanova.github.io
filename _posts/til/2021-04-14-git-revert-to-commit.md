---
title:  "Git: Revert to a previous commit"
description: "How to revert to a previous commit in history at once"
category: til
tags: git github
---

Note that this is like `reset` but for public branches.

In order revert to a previous commit in history `803cda1`:
```shell
git checkout -f 803cda1 -- .
```
Reset from HEAD the changes you do not want to revert. Commit:
```shell
git commit -m "Revert changes to commit 803cda1"
```
