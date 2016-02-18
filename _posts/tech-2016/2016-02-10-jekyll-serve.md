---
layout: post
title: "jekyll serve"
date: 2016-02-10 02:00:00 -0700
category:
  - tech
tags:
  - jekyll
---

When developing your jekyll site content, you will want to repeatedly run
jekyll to ensure that the conversion to static html files works "correctly".
(i.e. you haven't made any mistakes :-)) <!--more-->

~~~ bash
jekyll serve --watch
~~~

The command above will convert and serve the site from port 4000 so that
you can test it from a web browser. When it detects a change, it will
regenerate the site. For a site with a few hundred posts (such as this one)
it takes about 4 seconds to generate. When you are making or testing
changes, it feels like closer to 7 or 8 seconds. The difference between this
and the quicker methods below (< 1 second) is noticeable, and it's nice
to avoid the lag when possible.

~~~ bash
jekyll serve --watch --incremental
~~~

The command above watches for incremental changes. Though it does try
to regenerate all impacted content, I find that changes to pages that loop
through posts often do not get reflected properly. None the less, this is
useful when making changes to a single post or page (recent or old),
as it takes about 0.5 seconds for that use case.

~~~ bash
jekyll serve --watch --limit_posts 10
~~~

When making changes that impact a large number of the generated pages
(eg. layout files, include files, css files etc), it is nice to regenerate
the whole site. However, you don't need to regenerate every
single post. For this use case, you can limit the number of posts to some
small number to quickly test changes without the overhead of a full site rebuild.
For this site in it's current form, it takes 0.7 seconds with 10 posts,
and 0.8 seconds with 20 posts (it seems to scale linearly). This command
is also useful when making changes to recent posts (i.e. within the threshold
  specified by `--limit-posts`).

**This is my preferred method**, unless I am
specifically working with older posts (which is relatively uncommon).
