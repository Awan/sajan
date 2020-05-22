---
layout: post
comments: true
date: 2019-09-11
slug: dwm
title: dwm window manager
description: Tiling window manager that sucks less
tags:
- dwm
- windowmanager
- suckless

---
## What's **DWM**?

[DWM](https://dwm.suckless.org) is a Tiling window manager by [Suckless
community](https://suckless.org/).

### Installation

You can install **dwm** by using your distribution package maangers. But as
**dwm** is configured by hand before compilation, so it's recommended you clone
its repository, configure and then compile it for your system. I have a
[fork](https://gitlab.com/Abdullah/dwm.git) which you may like.

## Configuration

In the root directory, there is a file **config.h**. You can edit it how you
like. After editing run **make** and then as root (if you wanna install
as system-wide) or copy the **dwm** executable file to your path.

Let's take a look at my fork compiled **dwm**.

The default Modifier is Super Key (Windows key on most laptops). You can change it to Alt key or whatever you like.  From now on I'm using Mod for super key.

Let's open a window. The first window will always be in full screen.

![](/images/dwm-default.png)

Let's add more windows. I'll introduce you some terms used in Window Managers.
The larger area is called Master. When you open new windows, the first window is pushed to stack area. Take a look at this screenshot.

![](/images/dwm-2.png)

Add another terminal window.

![](/images/dwm-3.png)

If you wanna move the window in stack area to come back in Master area,
just focus it with <b>Mod + j/k</b> and then press <b>Mod + Shift +
Return</b>.

![](/images/dwm-move.png)

You can resize the increase/decrease Master area with <b>Mod + h/l</b>.

![](/images/dwm-resize.png)

For now, it's enough for you to get started. I'll update it soon. In sha
Allah.