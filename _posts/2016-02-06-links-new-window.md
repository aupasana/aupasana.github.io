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

~~~ html
<a href="http://www.contoso.com" target="_blank">contoso.com</a>
~~~

With the move to jekyll, I looked for a way to do this in markdown. Though it isn't supported by vanilla markdown, kramdown does support it.

<!--more-->

~~~ markdown
[contoso.com](http://www.contoso.com){:target="_blank"}
~~~

Though markdown is intended to simpler than html, I find links to be just as intrusive in markdown
as they are in html. I prefer named links with the ```href``` values to follow. i.e.

~~~ markdown
[contoso.com][a]

[a]: http://www.contoso.com
~~~

Unfortunately, I did not find a way to specify the ```target``` using this syntax with kramdown. 
All of this led to the following javascript snippet which opens non-domain links in a new window. 
Though I would have preferred to avoid more javascript, 
isolating this behaviour to one piece of javascript code meant that the markdown itself
was free of the ```target="blank"``` annotations. It ended up being the cleanest solution.

~~~ html
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
~~~