---
title:  "Git: Pull a GitHub Pull Request"
description: "How to pull locally a GitHub Pull Request"
category: til
tags: git github
---

To pull a GitHub Pull Request `pull/{ID}` into a local branch named `pr/{ID}`:

```shell
git fetch upstream pull/{ID}/head:pr/{ID}
```
