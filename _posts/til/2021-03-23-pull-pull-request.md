---
title:  "Git: Pull a GitHub Pull Request"
description: "How to pull locally a GitHub Pull Request"
category: til
tags: git github
---

To pull a GitHub Pull Request `pull/{ID}` into a local branch named `pr/{ID}`:

- [Fetch the reference to the pull request](
  https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/checking-out-pull-requests-locally) 
  based on its ID number, creating a new local branch:
  ```shell
  git fetch upstream pull/{ID}/head:pr/{ID}
  git checkout pr/{ID}
  ```
- Pull:
  ```shell
  git checkout pr/{ID}
  git pull upstream pull/{ID}/head
  ```
  ```
  warning: fetch updated the current branch head.
  fast-forwarding your working tree from
  ```

Note:
```shell
git fetch upstream pull/2178/head
```
```
 * branch              refs/pull/2178/head -> FETCH_HEAD
```