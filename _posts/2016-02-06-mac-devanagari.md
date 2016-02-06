---
layout: post
title: "Sanskrit editing on a mac"
date: 2016-02-06 11:00:00 -0700
tag:
  - mac
category: 
  - sanskrit
  - tech
---

Many text editors on a mac don't handle devanagari well. This is especially
true of code editors (eg sublime text and bbedit).

Two simple editors that work with devanagari text are <!--more-->
CotEditor and TextEdit. The later comes out of the box, but I avoided
it for a long time because it prompts you to open or create a new file
each time it is launched. (Contrast this with the behaviour of Notepad 
on Windows) Thankfully, this is easily modified:

~~~ bash
defaults write -g NSShowAppCentricOpenPanelInsteadOfUntitledFile -bool false
~~~

MacDown is designed for use with markdown files, and works with devanagari
text. This makes it well suited for blogging (it's what I'm using for
this post).

Pages and Microsoft Word both handle devanagari text well, but are too
heavyweight for simple editing tasks. 