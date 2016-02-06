---
layout: post
title: Open links in a new window
date: "2016-02-06 01:30:00 -0700"
comments: true
tag: 
- jekyll
- tech
- javascript
---

I like to have links to other sites and documents open in a new window. Using raw html, this is done with ```target="blank"```. i.e.

{% highlight html %}
<a href="http://www.contoso.com" target="_blank">contoso.com</a>
{% endhighlight %}

With the move to jekyll, I looked for a way to do this in markdown. Though it isn't supported by vanilla markdown, kramdown does support it.

<!--more-->

{% highlight markdown %}
[contoso.com](http://www.contoso.com){:target="_blank"}
{% endhighlight %}

Though I find markdown to be simpler than vanilla html, I find the html syntax to be intrusive. 
I prefer named links which don't interrupt the flow of the paragraph with inline ```href``` values. i.e.

{% highlight markdown %}
[contoso.com][a]

[a]: http://www.contoso.com
{% endhighlight %}

Unfortunately, I did not find a way to specify the ```target``` using this syntax with kramdown. 
All of this led to the following javascript snippet which opens non-domain links in a new window. 
Though I would have preferred to avoid more javascript, 
isolating this behaviour to one piece of javascript code meant that the markdown itself
was free of the ```target="blank"``` annotations. It ended up being the cleanest solution.

{% highlight html %}
  <script type="text/javascript">
    (function() {
        var links = document.links;
        for (var i = 0, linksLength = links.length; i < linksLength; i++) {
            if (links[i].hostname != window.location.hostname) {
              links[i].target = '_blank';
            }
        }
    })();    
  </script>
{% endhighlight %}
