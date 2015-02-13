---
layout: post
title: "Simple Blogging"
modified:
categories: 
excerpt:
tags: []
image:
  feature:
date: 2014-02-10T17:59:43+00:00
---

**This post is somewhat superceded by my partial move to [medium.com](https://medium.com/@tomreadings)**

A blog seems a sensible thing to have, if only so that I have somewhere to write longer posts for reference on twitter.

It gives me to put content I might want to share with someone, regardless of whether anyone finds it, or chooses to read it.

So I have decided to make a blog. Simple to start, pretty later.

The thing is, I have done this many time before, partly just to trial different platforms ([wordpress](http://wordpress.com/), [blogger](https://www.blogger.com), posterous, [svtle](https://svbtle.com/). Last time round I settled on posterous. For those of you (imaginary readers), that do not know, posterous was a blogging platform that linked in with services like twitter to spread your content across different channels. Unfortunately, posterous was bought out and closed down by twitter. I could have [moved my posts](http://techcrunch.com/2013/02/15/posterous-will-shut-down-on-april-30th-co-founder-garry-tan-launches-posthaven-to-save-your-sites/) on to ‘posthaven’, but it didn’t seem worth it. I am not a very frequent blogger, I didn’t have too many posts.

However, since the closure of my old blog I have found myself wanting to link to items that I had written up in some detail, and writing the posts up again was frustrating and incomplete. I realised that even a small amount of content can add up in value over time.

_Geek Alert - the following content will not be of interest to (admirably) low tech readers_

### Options for blogging

1.  sign up to another (free) blogging **service** (wordpress/blogger/tumblr)
2.  install a blog or cms myself (wordpress/statamic/etc)
3.  go geek and use a static site generator (Jekyll/Octopress/ruhoh/nanoc)

Predictably, I went with number 3. As a brief overview, rather than dynamically retrieving and rendering web content from a database (like wordpress etc), a static site generator creates simple HTML webpages to represent your content. It does this intelligently, making them look pretty and all, but the final result is a set of pages you could put on a usb stick and open in your browser, not requiring a webserver, database, etc.

#### Using a static site

The last time round I lost my content because it was wrapped up in someone elses platform and they decided to do something else with it. Thats fine, I’m not bitter (really!), but it served as a useful reminder - service providers have their own priorities. If I want to keep hold of my posts etc, I need to ensure that it remains accessible to me. If I generate a static site, those files are entirely under my control. They require only the most simple, cheapest, low maintenance web server to present them on the web, and I can fiddle with them on my computer offline to my heart’s content.

The reason I chose Jekyll as my static site generator (there are **so** [many](http://staticsitegenerators.net/) is that, fortuitously, [github](http://techcrunch.com/2012/07/14/what-exactly-is-github-anyway/) will do the generation bit for me, and host my site for free (I genuinely love github). This does mean I am relying on a service provider to look after my blog again, but in this case our priorities are aligned. Even if github decides at a later date that they no longer wish to display my blog, their entire business model is based on securely storing peoples code, regardless of its function. So my blog should still be there, and I can move it if I want. Because I am using github, which has a spendid API, I can also use a tool like [prose.io](http://prose.io) to create and edit my blog posts, if I would prefer to edit online.
