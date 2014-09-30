---
layout: post
title: New  Beginnings
category: general
tags: [Site]
---

It's been nearly five years since the last redesign of this site and I decided to try something new. Previous versions of my website were custom built in PHP and backed by a database. While this gave me unlimited possibilities it also meant that any small modification required a lot of time and effort. I have decided to ditch a dynamic website in favour of a static site built using [Jekyll](http://jekyllrb.com/) that, hopefully, will mean posting new articles will take less effort and happen more often.

<!-- more -->

I was able to get a basic website running in Jekyll that provided most of the functionality I wanted within a few hours. I needed some additional functionality so I wrote two plugins for Jekyll to add support for a [tag cloud](https://github.com/MitMaro/jekyll-tags-list-plugin) and to make [integration of code highlighting](https://github.com/MitMaro/jekyll-prism-plugin) with prism seamless. I will have blog posts on these in the future. I haven't really developed much with Ruby so the plugins might not be the best but I am always open to improvements. After getting the basic website running I switched from doing straight CSS to SASS along with the [Bourbon](http://bourbon.io/) mixin library. Bourbon was new to me but I have done work with SASS before so this wasn't much of a challenge.

Finally I used [GitHub](http://github.com/) pages to host the site, but because I use custom plugins that are not supported by GitHub I have to build the site manually. To accomplish this I created a source branch that contains the Jekyll site and have master only contain the static HTML pages.


