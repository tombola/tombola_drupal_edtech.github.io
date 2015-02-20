---
layout: post
title: "Custom Code in Drupal Content"
modified:
categories: drupal
excerpt:
tags: []
image:
  feature:
date: 2014-11-20T17:31:19+00:00
---

It is a generally accepted **bad idea** to give users the ability to put unfiltered javascript or any other code into their content. It could cause any number of issues with the site, including security, and (especially within wysiwyg content) it is really hard to track down where the code is and what it was supposed to do.

Having said this, with limited resources and supporting a large number of administrative users, I often find that I often have edge cases where we want some slightly custom layout or embedded content to be shown _within_ content that is managed by a non techy user. This edge case might be re-used and become a staple part of the site/theme, at which point it is worth considering the ‘right way’ to implement it, using a new field, a wysiwyg dialogue or something similar.

## Example

As a very simple example - within a bootstrap based theme the administrators of several different (landing) pages have asked if I can add ‘Call to Action’ buttons for appointment booking etc, in the same way I have done on the homepage (by styling a menu). The buttons really need to be placed in context within the body text, rather than just plonked at a specified place on every page, so in the first instance I can’t necessarily just create a multiple instance field, or a menu block. With a bit more extended investigation I could work out several most likely scenarios and create different Display Suite layouts to position the content*, but as yet I don’t know if this will ever be repeated.

The page owner needs to be able to continue to edit the content easily and move the snippet/component around without coming to me. It **might** also be useful, on occasion, to use PHP code to configure some of these custom content elements (I know, I know!), but also they should allow for script inclusion etc (for infographics etc). So basically this involves an unfiltered code block(!).

## Solution?

I was mulling all this over and I have a possible solution in mind which would allow me to provide custom code, but still allow the admin to move it around in their content (without breaking).

The proposed solution is to add a **field** to the node type, accessable only by a selected developer role. It would accept multiple instances of unfiltered code, each associated with a machine readable key. An **input filter** would swap instances of **[widget:key]** in the body (or other text field) with the provided code. A checkbox would enable each snippet, allowing for it to be individually disabled for troubleshooting.

The objective is low overhead for me to create quick customisations (prior to consolidating into planned features). This would hopefully allow me to avoid technical debt created by creating over-engineered solutions to one time problems, or hacking components around later once I see how they are being used. I should be able to easily locate problem code, and disable all/individual snippets without disrupting the site too much. Because the custom snippets of code each stored in a field, instances can be tracked down via the database to work out which deserve consolidation, or are problematic.

I already have the start of a niggling feeling that this approach might not work out as expected long term, but I think I might try it out on a peripheral site and see how it pans out.

* _I don’t want to use panels - it seems like vast overkill for the majority of the page layouts we are considering, and in my opinion would add an additional administrative burden._
