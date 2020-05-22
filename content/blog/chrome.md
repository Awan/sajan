---
author: Abdullah
layout: post
date: 2019-09-15
title: 'Google Chrome for deiban and derived distributions'
slug: chrome
comments: true
description: 'How to install google chrome in Debian based distributions'
tags:
  - chrome
  - google
  - google-chrome
  - chrome_in_linux
---

You'll have to admit google chrome is super fast. Along with other plugins I love to use it as main browser. But unfortunately it isn't in debian repositories.

So how to install it? Here is the procedure you can follow to get
latest chrome from google. 

```
$ echo 'deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main' | sudo tee -a /etc/apt/sources.list > /dev/null
$ sudo apt update
$ sudo apt install -y google-chrome-stable
```

Enjoy using Chrome.
