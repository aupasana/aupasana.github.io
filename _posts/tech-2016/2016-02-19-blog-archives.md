---
layout: post
title: "Blog archives and list.js"
date: 2016-02-19 02:00:00 -0700
category:
  - tech
---

The very nature of blogs -- especially those that are topic specific --
necessitates archives. Most blogs have archives by date, category and tag.
Recently, I took a different approach.

Why bother with slicing and dicing data in different ways, when
you can have a single list that facilitates dynamic searching and ordering
... all on the client side with a lightweight library?

Given that most blogs don't have thousands of posts, client side searching
of the entire blog metadata (i.e. title, date, category and tags) is feasible
on modern mobile devices.

On this site, I've used [list.js][js], a library that supports filtering and
ordering on lists and tables (based on arbitrary html classes). And pagination
support is available (through an extension). Using it is simple, and the
[list.js][js] documentation and samples are good. I'm surprised that more
blogs don't take a similar approach.


[js]: http://www.listjs.com
