---
author: Abdullah
title: Terminal Sharing service
description: Terminal Sharing service
slug: tmate
date: 2020-05-17
comments: true
layout: post
toc: true
tags: [ tmate, terminal sharing, remote, rdp, terminal sharing software ]

---

## What's tmate?

On *nix systems, sometimes we need support. And geeks don't like GUI apps just
to have your system in front of them, at least I don't like that :wink:

[tmate](https://tmate.io) is terminal sharing software you can use it to
connect with your friends and you both work from there. 
It's available in many distributions repos and in case you aren't lucky
enough, you can compile it from source or there are pre-compiled binaries
there in their Github page.

## How to use?

Once installed, just invoke `tmate` from command line.
tmate needs an ssh key so in case you don't have an ssh key, generate one.

```
ssh-keygen
```

Once ready, invoke tmate. It will start connecting to its server and show you
in status bar once connected. 
You can now show the URIs by `show-messages` command.

```
tmate show-messages
```

It will provide you both [web, ssh] priviliged and non-privileged links.
Share with your friends how you like. 

Enjoy!

