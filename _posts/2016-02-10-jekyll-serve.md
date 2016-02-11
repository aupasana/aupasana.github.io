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
(i.e. you haven't made any mistakes :-))

~~~ bash
jekyll serve --watch
~~~

The command above will convert and serve the site from port 4000 so that
you can test it from a web browser. When it detects a change, it will
regenerate the site. For a site with a few hundred posts (such as this one)
it takes about 4 seconds to generate. When you are making or testing
changes, it feels like closer to 7 or 8 seconds.

~~~ bash
jekyll serve --watch --incremental
~~~

The command above watches for incremental changes. Though it does try
to generate all impacted changes, I find that changes to files that loop
through posts often do not get reflected properly. None the less, this is
useful when making changes to a single post (recent or older), as it takes
about 0.5 seconds for that use case.

~~~ bash
jekyll serve --watch --limit_posts 10
~~~

When making changes that impact a large number of the generated pages
(eg. layout files, include files, css files etc), it is nice to regenerate
the whole site. However, you don't need to regenerate every
single post. For this use case, you can limit the number of posts to some
much smaller number to quickly test your changes without a full site rebuild.
For this site in it's current form, it takes 0.7 seconds with 10 posts,
and 0.8 seconds with 20 posts (it scales about linearly). This is also
useful when making changes to recent posts (i.e. within the threshold
  specified by `--limit-posts`).

The difference between 0.5 seconds and 4 seconds is noticeable, and it's
nice to be able to avoid the lag when possible.
