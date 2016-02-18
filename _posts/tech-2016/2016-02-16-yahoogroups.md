---
layout: post
title: "yahoo group mails"
date: 2016-02-16 02:00:00 -0700
category:
  - tech
tags:
  - yahoogroups
---

There are a number of older yahoo groups with useful mails. Unfortunately,
the current interface makes it very difficult to search. This post describes
how to download the mails into a standard mbox. <!--more-->

First, download the prerequisites with brew (on a mac) or your favorite
package manager.

~~~ bash
brew install dash
brew install cpanm
brew install procmail
sudo cpanm -v JSON
~~~

Next, download the [mbox_yahoo](http://www.usenix.org.uk/content/yahoo_mbox.html) scripts.

The heart of the download shell script is this excerpt which shows the "magic" URL.

~~~ bash
for i in $( seq $MIN $MAX ) ; do
	curl -4 https://groups.yahoo.com/api/v1/groups/${GROUP}/messages/$i/raw > message_$i ;
	sleep 1;
done ;
~~~

The decode.pl script (from the same link) extracts the ygData.rawEmail portion
of the json encoded data.

~~~ perl
#!/usr/bin/perl
use JSON;
use Data::Dumper;
use HTML::Entities;

# 20140512 (ed@s5h.net)
# this script helps get mail back from the evil clutches of yahoo.
# do whatever you want with it

binmode STDOUT, ':utf8';
my $json = <>;

if( $json !~ /^{"ygPerms":/ ) {
	die "no can do, buckeroo";
}

my $entity = decode_json( $json );

my $message = join( "", split( /
/, $entity->{'ygData'}->{'rawEmail'} ) );
print decode_entities( $message ), "\n";
~~~

Stitching together decode.pl and formail (a part of procmail)
gives us a standard mbox.

~~~ bash
cat message* | perl decode.pl | formail >> archive.mbox
~~~
