---
author: Abdullah
comments: true
date: 2020-05-10
slug: site-as-git-repo
description: "How to manage a website using git"
title: "How to manage a website using git"
layout: post
---


Git is another awesome tool developed and maintained by Linus Torvalds who wrote linux kernel. In this post I'll explain how can we use it for our site maintenance. I have a vps on which my site is hosted along with a mail server, git server and a web server too. But I'm sure this guide can be used with shared hosting accounts with some modifications.

Install git. Once installed, as root user, create git user and add it to www-data group.

```
useradd git -m -G www-data
```

Login into this new git user.


```
su - git

```

Create an ssh directory for this account.

```
mkdir .ssh
```

Upload your user ssh public key to this directory how you want. I use pastebin here. Assuming you pasted your public key somewhere on pastebin, I'll fetch it using curl.

```
curl -o .ssh/authorized_keys 'pastebin address where you pasted the public key'
``` 

Create a directory for your user you wanna use for your site or this user maybe the one you use to login to your vps using ssh. I'll use user z for this post.

```
cd && mkdir z && cd z

```

Create a git repo here now.

```
git init --bare mysite.git

```
Create a hook in .git directory.

```
echo "#!/bin/sh \
cd /var/www/html \
unset GIT_DIR  \
git pull \ " > ~/z/mysite.git/hooks/post-receive && chmod +X ~/z/mysite.git/hooks/post-receive

```
That's it. Now go to the directory where your site is hosted, in this example we used /var/www/html for site and z as username which is used to maintain our site in future using git like in above hook we used that. You can modify both hook and here this code too according to your needs.
```

cd /var/www/html && git clone ~/z/mysite.git && cd mysite.git && mv * /var/www/html/ &&  cd /var/www/html && rm -rf mysite.git
```

We have made it. Now in your local machine, clone this repo this way.

```
git clone 'your vps ip or domain if it's pointed to your vps':z/site.git

```
cd into the directory you just cloned, do some modifications and push the changes and you'll see the magic. If you have some problems just ping me and I'll be glad to help.
