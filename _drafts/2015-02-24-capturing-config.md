---
layout: post
title: "Making a Drupal Distribution #2"
modified:
categories: drupal
excerpt:
tags: []
image:
  feature:
date: 2015-02-24T16:27:04+00:00
comments: yes
---

#Capturing Drupal Config

My [previous post](http://tombola.github.io/drupal/making-a-drupal-distribution/) describes the whys and wherefores.

So I have a heavily commented make file with my modules in it, and a development environment with some workflow scripts etc which will allow me to repeatedly test my install profile as I build it up. Now I can start making my distribution actually work.

<div class="post__update"></div>

I mentioned in the last post that I wanted to test my install profile on the same codebase as an existing dev site. This used drupal [multisites](/drupal/making-a-drupal-distribution/#multisite) to separate the databases. As a side note, multisites caused issues with my [unattended](/drupal/making-a-drupal-distribution/#unattended) workflow. I shouldn't imagine this would give anyone else sleepless nights, so I will gloss over it, though here is my [problem/solution](/drupal/2015-02-24-unattended-multisite/) if you are interested.


<a class="btn btn-info" href="/drupal/making-a-drupal-distribution">Previous step</a>
<a class="btn btn-info btn-disabled">Next installment</a>



<!--href="/drupal/2015-02-24-capturing-config/"-->