---
author: Abdullah
layout: post
date: 2020-05-08
slug: wallpaper-automation
comments: true
tags:
- wallpapers
- automation
- systemd
- systemd timer
- systemd unit
description: "Automate the boring stuff of wallpapers with systemd"
title: "Automate the boring stuff of wallpapers with systemd"
---

So assuming you're not using a DE and don't wanna install a tool which comes
with a lot of dependencies just to automate the boring stuf of changing
wallpapers (root window of Xorg). I wrote a simple Python
[program](https://github.com/Awan/beautify.git) which you can use as systemd
unit too.

Clone the [repository](https://github.com/Awan/beautify.git) or download/copy
the beautify.py if you don't want systemd part. I'd recommend ~/bin for such
executable scripts. You can execute it from _.xinitrc_ or _.xprofile_. For
systemd there is explaination in repository readme file too.

```
git clone https://github.com/Awan/beautify.git
cp beautify/beautify.py ~/bin/beautify
cp beautify/systemd/beautify.service ~/.config/systemd/user/default.target.wants/
systemctl enable --user beautify.service
systemctl start --user beautify.service
```

Don't forget to edit the beautify.service. Add path
to beautify script where you copied it, and also add
your wallpapers collection's path and duration.

If you wanna execute it without systemd, you can
copy the _beautify.py_ to ~/bin and execute it from
_~/.xinitrc_ or _~/.xprofile_ like this.


```
cat ~/.xinitrc
...

~/bin/beautify ~/pix/wallpapers 300
...

```

It will change the wallpapers from _~/pix/wallpapers_ every 5
minutes. Enjoy!
