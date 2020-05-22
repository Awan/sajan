---
author: Abdullah
slug: contribution-with-git
title: How to contribute to open source project
description: How to contribute to a project using git
date: 2020-02-12
comments: true
layout: post
tags:
  - contribution
  - git
  - github
  - fork
  - repository
toc: true
---

So you want to contribute to some open source project which is hosted on
git[hub,lab] or some other git website.
Here is all you want to do.

## Fork the repository

Create a personal fork. On github, visit the project repository and hit fork.
It will fork the project in your personal account.

## Clone it

Clone it in your local machine so you can work on it.
Remember you are cloning the fork, and not the original project.

```
$ git clone git@github.com:USERNAME/project
```

## Add the upstream

Add the original project as upstream.

```
$ git remote add upstream
https://github.com/ORIGINAL_PROJECT_USERNAME/ORIGINAL_PROJECT_REPO
```

## Fetch latest work

If you forked a project just now, you can go to next step. If there is a time
gap, fetch latest work from upstream to your fork.

```
$ git pull upstream
```

## Create a new branch

Create a new branch so you can work there.

```
$ git checkout -b develop
```

## Add your contribution

Add your work in new created branch. 
Commit changes. Make sure to write meaninigful commits.

## Push your work live

Push the changes you have made to remote origin.

```
$ git push
```

## Create a pull request

Go to your fork page and create a pull request. That's it


