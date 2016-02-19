---
layout: page
title: Stardict
toc: true
---

Most platforms and mobile devices have apps which understand the "stardict" dictionary format. As a result, you can easily add new stardict dictionaries, and search them. Here, you will find stardict files for sanskrit dictionaries (monier-williams, apte), and grammar texts. The input format is a simple subset of the itrans scheme. It is designed for ease of input on mobile devices, and should be relatively natural.
input scheme

~~~
a aa i ii u uu R Rii L Lii e ai o au am aH

ka kha ga gha Na
cha Cha ja jha na GYa
Ta Tha Da Dha Na
ta tha da dha na
pa pha ba bha ma
ya ra la va
sha Sha sa ha
La xa
~~~

Note: this input scheme is a variation of the itrans format. It purposely omits all punctuation, which makes it easy to type on mobile devices. Since stardict applications generally accept case-insensitive input, searching becomes simple, while remaining almost lossless.

## Dictionary files

* [[ link ][apte]] apte sanskrit to english dictionary
* [[ link ][aptebi]] apte sanskrit to english dictionary (with reverse lookup)
* [[ link ][mw]] monier-williams sanskrit to english dictionary
* [[ link ][mwbi]] monier-williams sanskrit to english dictionary (with reverse lookup)
* [[ link ][amara]] amara-kosha with contextual information (this is experimental and has errors)
* [[ link ][shabda]] shabda kalpadruma sanskrit to sanskrit dictionary
* [[ link ][vacha]] vachaspatyam sanskrit to sanskrit dictionary

## Vyakarana files

* [[ link ][dhatu]] dhātupātha (processed version from sanskritdocuments.org)
* [[ link ][lsk]] laghu siddhānta kaumudī
* [[ link ][bala]] bālamanoramā
* [[ link ][tb]] tattvabodhinī
* [[ link ][kasika]] kāśikā
* [[ link ][nyasa]] nyāsa

[apte]: {{site.filecabinet}}/stardict/apte.tar.gz
[aptebi]: {{site.filecabinet}}/stardict/apte-bi.tar.gz
[mw]: {{site.filecabinet}}/stardict/mw-itrans-dev.tar.gz
[mwbi]: {{site.filecabinet}}/stardict/mw-bi-itrans-dev.tar.gz
[amara]: {{site.filecabinet}}/stardict/amara-context-2.tar.gz
[shabda]: {{site.filecabinet}}/stardict/kalpadruma.tar.gz
[vacha]: {{site.filecabinet}}/stardict/vachaspatyam.tar.gz

[dhatu]: {{site.filecabinet}}/stardict/dhatupatha.tar.gz
[lsk]: {{site.filecabinet}}/stardict/laghu-kaumudi.tar.gz
[bala]: {{site.filecabinet}}/stardict/balamanorama.tar.gz
[tb]: {{site.filecabinet}}/stardict/tattvabodhini.tar.gz
[kasika]: {{site.filecabinet}}/stardict/kashika.tar.gz
[nyasa]: {{site.filecabinet}}/stardict/nyasa.tar.gz


## Installation

* on iOS, use the "dictionary universal" applicaiton
* on android devices, use the "colorDict" application
* on windows, use the "goldendict" app
* on mac osx, use the "goldendict" app

## Sources

The files above were processed from various sources

* The now defunct http://www.sansknet.org website
* [[ link ][sandic]] Sandic project at Sourceforge
* [[ link ][koeln]] Sanskrit Lexicon at Koeln

[sandic]: http://sourceforge.net/projects/sandic/
[koeln]: http://www.sanskrit-lexicon.uni-koeln.de/index.html
