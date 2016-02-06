---
layout: post
title: Working with jekyll
date: "2016-02-02 07:30:00 -0700"
comments: true
tag: 
- jekyll
- tech
---

Migrating this site to jekyll has been an interesting experience.
In order to simplify the deployment process, I stuck to vanilla jekyll 
(i.e. what was supported by github pages). Here are some learnings:

<!--more-->

+ The built-in pagination support is inflexible and lack-luster. Want to manage two 
logical blogs on indepenent topics in a single deployment? Forget about it.

+ Something as simple as adding a table of contents to a page is more painful than it 
should be, unless you are looking for simple in-line positioning. I ended up using 
the jQuery TOC library.

+ There is little support for post tags or categories in combination with
pagination. Creating tag / section specific pages is not possible.

The primary workaround for this is to have a single page with all posts sorted by tags.
Because this scales poorly, it's best to have just the titles, or a very limited extract
for each post.

## Get a list of sorted tags.

~~~ liquid 
{% raw %}
{% assign sorted_tags = (site.tags | sort:0) %} 
{% endraw %} 
~~~

## Create a list of all posts, grouped by tag

~~~ liquid
{% raw %}
{% for tag in sorted_tags %}
	{% assign t = tag | first %}
	{% assign posts = tag | last %}

	{{t | downcase}}
	{% for post in posts %}
	  {% if post.tags contains t %}
	  	{{ post.date | date_to_string }}: {{ post.title }}
	  {% endif %}
	{% endfor %}
{% endfor %}
{% endraw %}
~~~

Adapted from [jokecamp.com](http://www.jokecamp.com/blog/listing-jekyll-posts-by-tag/)


