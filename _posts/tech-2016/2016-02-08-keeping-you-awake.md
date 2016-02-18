---
layout: post
title: "Keeping You Awake"
date: 2016-02-08 02:00:00 -0700
category:
  - tech
tags:
  - mac
---

There are times when you don't want your macbook to go to sleep.
This is typically related to long-running slow downloads, or other
long-running background tasks.

There are a few different solutions to this. <!--more-->
The simplest solution is
the [KeepingYouAwake][git] app. It is an open-source caffeine clone that
runs in the taskbar and makes toggling power settings simple.

If you want to avoid running yet another application, you can use the
built-in support that comes with every macbook. Simply run the following
command on a terminal, and ```ctrl-c``` to break out when you're done.

~~~ bash
pmset noidle
~~~

I like KeepingYouAwake -- it's a simple application that's easy to use,
and it's icon makes the current setting clear. There have been times when
I've set the noidle setting, and forgotten about it. The reminder in the
taskbar is nice.

[git]: https://github.com/newmarcel/KeepingYouAwake
