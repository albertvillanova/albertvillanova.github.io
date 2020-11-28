---
title:  "Commit and Push using GitHub Actions"
description: "How to commit and push using GitHub Actions"
category: til
tags: github-actions
---

It is possible to [commit and push using GitHub Actions](
https://github.com/actions/checkout#push-a-commit-using-the-built-in-token):

```yaml
name: Commit and push
on: push
jobs:
  report:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Create report file
        run: date > report.txt
      - name: Commit and push report
        run: |
          git config user.name github-actions
          git config user.email github-actions@github.com
          git add .
          git commit -m "Generate automated report"
          git push
```
