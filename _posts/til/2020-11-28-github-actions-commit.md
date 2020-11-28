---
title:  "GitHub Actions: commit and push"
description: "How to commit and push from GitHub Actions"
category: til
tags: github-actions
---

It is possible to commit and push to origin from GitHub Actions:

```yaml
name: Push commit
on: push
jobs:
  report:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Create report file
        run: date + %s > report.txt
      - name: Commit and push report
        run: |
          git config --global user.name 'Your name'
          git config --global user.email 'your-username@users.noreply.github.com'
          git commit -am "Automated report"
          git push
```
