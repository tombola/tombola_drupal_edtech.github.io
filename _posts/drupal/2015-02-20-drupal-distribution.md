---
layout: post
title: "Drupal Consolidation"
modified:
categories: drupal
excerpt:
tags: []
image:
  feature:
date: 2015-02-20T11:19:07+00:00
---

## Where I am at

I have been intermittently working with a drupal 7 multiple site 'platform' for several years, which originally emerged from a single site. I am the sole maintainer. The platform is not based on a drupal 'multi-site' configuration, as the shared codebase model seemed more hindrance than feature. Instead the (four) sites share a common pattern of base configuration, each cloned (direct copies of files and db) from an early version of the build. A set of custom modules is kept up to date as one git repo that is cloned into each of the sites. Similarly a base theme, and sub themes for all of the sites are also held in a single repo and cloned into each site. More recently, I created an entirely separate site to aggregate and index these sister sites (via feeds) to provide a more advanced, yet loosely coupled [search facility](https://github.com/fxplus/search_apex).

The setup as described was intended to make maintaining these sites simpler, as extended functionality could be built into some sites whilst the other sites are left without the baggage of additional modules and configuration, making them more easily performative, and simpler to maintain. Sister sites can optionally share any new features, because the early build decisions are shared, so configuration is transferable, and custom modules/features from the shared repo can simply be turned on. I opted not to construct a single site segmented by Spaces, or equivalent pattern, because initially it was not clear how far the sites might diverge from one another.

This workflow has seemed to make a rough kind of sense until now, but I am returning to the decisions I made when creating the platform to try and get it ship shape now that each site has largely settled into a stable pattern of usage. I want to make sure that I have not incurred an impractical amount of technical debt, and that site maintenance is transferable, should it need to be. Another consideration is the approach of Drupal 8. When this transformative version is widely used, it will be **much** easier to migrate simplified, minimal sites. 

## Why rock the boat?

Drupal is endlessly configurable. A lot of this configuration is executed through the admin interface and captured in the database. This oft criticised lack of separation between configuration and content should soon be [alleviated](https://www.drupal.org/documentation/administer/config) by the adoption of Drupal 8, but for the moment (maybe until the end of 2015?) it does not seem sensible to move to D8.

The sites I have created have evolved to meet the requirements of their users. Due to reactive (and sometimes undocumented) measures taken in individual sites sometimes similar workflow and layout objectives have been achieved in subtlely different ways. Earlier in the process, these changes were captured in Drupal Features as much as was possible, but this became complex in itself.

Now that I can see the way these sites are being used, and content/design policies have emerged that structure (admin) user's interactions consistently across each site, I believe I should be able to redistribute the content and processes, largely into one large site (still using multiple domains). Where large sets of unique functionality must be preserved, it will be **these** aspects that become their own sites. Some of these peripheral functions will have pushed outside the cms envelop, and may no longer need to be based on drupal at all, though housed (sym-linked) in a sub directory within the drupal installation. Hopefully once I have also detached the design components from the drupal theme I will be able to preserve consistent user experience regardless of the underlying system.

The result of this detachment process will hopefully be that I have a nearly out of the box drupal installation, with configuration simple enough to be captured in code 

