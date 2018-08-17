---
layout: single
title: "Jekyll plugin for Prism"
date: 2014-10-04 08:30:00 -0230
categories: development
tags: [Jekyll, Ruby, Prism.js]
---

This post was migrated from an older version of the blog.
{: .notice--warning}

As a software developer, I require excellent support for syntax highlighting in a blogging platform. This blog uses
[Jekyll] as a platform and it has two options for syntax highlighting, [Pygments] and [Rouge]. Pygments is written in
Python and supports over 100 languages but it didn't have a few of the features I was looking for in syntax
highlighting. The Ruby-based Rouge seems to have many features but was very limited by Jekyll's implementation. Given
that the defaults of Jekyll didn't work for me I decided to go with what I was familiar with: a Javascript based syntax
highlighter. Specifically, I decided to use [Prism], which has hooks for plugins, uses standard markup and support for
all the languages I would need. Since I try my best to not mix HTML into the Markdown these posts are written in, I
decided to write a small plugin to add support for Prism to Jekyll.

There are a few existing plugins that already try to add Prism support to Jekyll, most notably a
[plugin][jekyll-prism-plugin] by [Garrett Murphey]. At the time of this post, Garrett's plugin hasn't been updated for
well over two years (aside from README updates) and also didn't support the plugins that can be downloaded with Prism.
I started trying to extend upon Garrett's work to add the extra features but ended up writing the whole plugin from
scratch. His plugin wasn't written as a Ruby gem and I didn't particularly like the HTML he generated.  The plugin I
developed supports all the plugins from the Prism website, is available as a gem, includes tests and since it's going to
be used on this blog will be kept up to date.

As I am new to development in Ruby and it is only the second time I have written a Ruby gem, I am sure there are many
things I did poorly or just wrong. Most notably, I am fairly sure I didn't do the dependencies correctly in my gemspec.
As I stated above the plugin is available on [RubyGems] if you want to try it out. There is documentation on the
[GitHub project page], where you can also grab the code. Feel free to fix any issues and send me a pull request and I
will be glad to include it. Please leave any criticism about the plugin below in the comments section and I will do my
best to respond.

[Jekyll]:http://jekyllrb.com/
[Pygments]:http://pygments.org/
[Rouge]:https://github.com/jneen/rouge
[Prism]:http://prismjs.com/
[jekyll-prism-plugin]:https://github.com/gmurphey/jekyll-prism-plugin
[Garrett Murphey]:https://github.com/gmurphey
[RubyGems]:https://rubygems.org/gems/mm-jekyll-prism
[GitHub project page]:https://github.com/MitMaro/jekyll-prism-plugin
