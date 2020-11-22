---
title:  "User/Organization GitHub Pages sites using fastpages"
description: "Added support for creating user/organization sites in GitHub Pages using fastpages"
category: til
tags: fastpages github-pages
---

Previously, GitHub only allowed **user/project sites** to set the repository default branch as their publishing source.
This was the main reason why **fastpages** could not be used to create user/project sites, as its automation deployment uses the `gh-pages` branch instead.

But now this is no longer the case: you can set the `gh-pages` branch as the publishing source for your user/organization site.

Thus, **fastpages can be used to create user/organization sites**.

I have made a [Pull Request](https://github.com/fastai/fastpages/pull/456) to adapt the fastpages setup for user/organization sites.
Once it will be merged, fastpages support for user/organization sites will be official.
