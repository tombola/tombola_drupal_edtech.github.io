---
layout: category-index
title: "Drupalisms"
date: 
modified:
excerpt:
tags: []
image:
  feature:
category: drupal
---


<!--<h1>{{ page.category }}</h1>-->

Here are some things I have writ about my experiences with drupal.

{% for post in site.categories.['drupal'] %}  
  {% include _teaser.html %}
{% endfor %}