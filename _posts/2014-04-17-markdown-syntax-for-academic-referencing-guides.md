---
layout: post
title: "Markdown Syntax for Academic Referencing Guides"
modified:
categories: 
excerpt:
tags: []
image:
  feature:
date: 2014-04-17T17:36:42+00:00
---

Following on from a previous post, I have made a simple drupal module to provide an extension to markdown.

The point of the module is to allow academic support to create and edit highlighted referencing examples for the myriad of referencing examples that crop up with students. The examples display with consistent highlights and ‘tooltips’ for each element of the reference.

As an example, if you write the following in the editor:

{% highlight html %}
{% raw %}
Reference:
>[THOMPSON, E. P.|author] [1966|year]. *[The Making of the English Working Class|title]*. [New York|place]: Vintage Books. 
{% endraw %}
{% endhighlight %}


Then the resulting page will display as follows (the black tooltip is on hover):
![referencing highlights]({{ site.url }}/images/content/referencing_highlights.png)

