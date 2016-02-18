---
layout: post
title: "jekyll serve --host"
date: 2016-02-11 02:00:00 -0700
category:
  - tech
tags:
  - jekyll
---

Sometimes, you'll find the need to test the jekyll output in
multiple environments. Recently, I encountered strange layout
behaviours which reproduced only in chrome on windows
(and not in chrome on mac osx). <!--more-->

To debug this, I started my Windows VM, and attempted to connect
to port 4000 on my host machine. Addressing it as `localhost`,
or the gateway ip from the VM, or the public ip of the host machine
... none of them worked.

It turns out that by default, jekyll serve only binds to the loopback
device, which is not addressable from other machines. Adding the option
`--host 0.0.0.0` to the `jekyll serve` command caused it to bind to
all devices, such that it was addressable from my VM
(using the host's **public** ip address).
