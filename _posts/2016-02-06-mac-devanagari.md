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

Two simple editors that work with devanagari text are
CotEditor and TextEdit. The later comes out of the box, but I avoided
it for a long time because <!--more-->
it prompts you to open or create a new file
each time it is launched. (Contrast this with the behaviour of Notepad
on Windows) Thankfully, this is easily modified:

~~~ bash
defaults write -g NSShowAppCentricOpenPanelInsteadOfUntitledFile -bool false
~~~

MacDown is designed for use with markdown files, and works with devanagari
text. This makes it well suited for blogging. Atom is an open-source editor
that works well unlike most of it's brethren (i.e. Sublime Text and BBEdit).

Pages and Microsoft Word both handle devanagari text well, but are too
heavyweight for simple editing tasks.
