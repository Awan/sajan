---
author: Abdullah
layout: post
title: "How to use vIM as IDE in Debian, Ubuntu, Mint"
date: 2019-10-11 
slug: vim-as-IDE
comments: true
toc: true
description: 'How to use vIM as IDE'
tags:
  - vim
  - editor
  - visual
  - text editor
  - vi
  - IDE
  - youcompleteme
---

Been using source based distributions for a long time. Source based distributions are cool for systems with limited resources. But what if you don't have enough time?

Debian is one of the oldest distribution there which is known for
stability. Stability? Well that never had been a priority for me but
for some reasons I came to it and now using it for some months. It's
a cool distribution.

Well, that enough said, let's come to the topic. vIM has been my
editor since I started using Linux. There are many other text
editors like nano but I never been interested in them. To be honest
still I only know how to exit from nano when a command is run by me
and nano was the default editor there.


I have been maintaining my
[dotfiles](https://gitlab.com/Abdullah/cfg.git) no matter which distribution I was using. But still I had to compile things for vIM and other cool software I use in my daily routine.


I was looking for some tool using <i> apt search </i> and found
<b> vim-youcompleteme </b> in search results. Which leaded me to
install it. I installed it and it also installed its dependencies.
In other distros I had been using before I manually had to compile
vIM and YouCompleteMe plugin. So here is the process you can follow
to have vIM with your plugins.


### Installing vIM 

Debian is a decent distribution. It has many flavours of
packages. If you don't want some extra features for some package,
you can have lightweight one. Others can have it how they want it to
be. Debian vIM is a light package. If you wanna use YouCompleteMe
vIM plugin, you must install vIM with extra features compiled. But
don't worry, Debian has it. Assuming you want vIM as your default
editor, these commands will install vIM, remove vIM with less
features and make it default editor. 


Remove vIM if you have it.

```
$ sudo apt remove vim vim-runtime gvim vim-tiny vim-common vim-gui-common vim-tiny vim-common vim-gui-common 
```

Install vIM.

```
$ sudo apt install vim-nox
```
Install Addon Manager.You can use plugins without a plugin manager too but it really makes your life easier.

```
$ sudo apt install vim-addon-manager vim-youcompleteme
```

Make vIM your default editor. 

```
$ sudo update-alternatives --set editor /usr/bin/vim.nox
$ sudo update-alternatives --install /usr/bin/vi vi /usr/bin/vim.nox 1
$ sudo update-alternatives --set vi /usr/bin/vim.nox
```


### Configure vIM

After everything is installed, now you can configure vIM to use these plugins. For example, I use <i>vim-youcompleteme</i>.

```
$ vam install youcompleteme
```

That's it. You can always have a look at my
[dotfiles](https://gitlab.com/Abdullah/cfg.git)
if have some issues. Enjoy using vIM.
