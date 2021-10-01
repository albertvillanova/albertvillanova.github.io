---
title:  "Git: Install a GitHub Pull Request"
description: "How to install a GitHub Pull Request"
category: til
tags: git github
---

To install a GitHub Pull Request:
```shell
python -m pip install git+ssh://git@github.com/{org-or-username}/{repo}.git@refs/pull/{ID}/head#egg={package-name}
```

Example:
```shell
python -m pip install git+ssh://git@github.com/huggingface/datasets.git@refs/pull/2324/head#egg=datasets
```
