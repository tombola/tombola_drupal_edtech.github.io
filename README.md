#tombola.github.io

Blog for technologist Tom Readings

For help with the theme, see [minimal-mistakes](http://mmistakes.github.io/minimal-mistakes/theme-setup/). This is also accessible from the local blog (http://127.0.0.1:4000/theme-setup/).

Because this theme uses ruby gems to do things like code syntax hightlighting, you will need to 

    bundle install

and serve it using

    bundle exec jekyll serve

rather than the normal

    jekyll serve

**Important** - when testing locally amend _config.yml ``url`` (comment out) to navigate the local site rather than skipping off to github.


###Navigation

change the navigation links at _data/navigation.yml

###Posting

    octopress new post "Title of post"

###Design

Use [Grunt](http://gruntjs.com/getting-started) to perform minification etc. Look at the Gruntfile for details. Jekyll should handle the sass itself.

**Remember** - the local site will be loading css from github (and your sass changes will not be reflected) if you forget to change config url (above).

###Dissemination

Some posts from this blog are to be aggregated by [Drupal Planet](https://www.drupal.org/planet). If a post is [suitable](https://www.drupal.org/planet/guidelines) for this purpose, **tag** it with *drupalplanet*, and it will be included in the rss at drupalplanet/feed.xml.