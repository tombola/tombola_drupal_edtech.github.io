---
layout: category-index
title: "Drupalisms"
date: 
modified:
excerpt:
tags: [drupalplanet]
image:
  feature:
category: drupal
---


<!--<h1>{{ page.category }}</h1>-->

Here are some aphorisms and conjecture regarding Drupal, written for aggregation by Drupal Planet.

{% for post in site.categories.['drupal'] %} 
{% if post.tags contains "drupalplanet" %} 
  {% include _teaser.html %}
{% endif %}
{% endfor %}