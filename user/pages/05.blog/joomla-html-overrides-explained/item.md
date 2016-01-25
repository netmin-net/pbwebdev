---
# http://learn.getgrav.org/content/headers
title: Joomla HTML Overrides Explained
slug: joomla-html-overrides-explained
# menu: Joomla HTML Overrides Explained
date: 20-05-2012
published: true
publish_date: 20-05-2012
# unpublish_date: 20-05-2012
# template: false
# theme: false
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration-status: review
    category: [Joomla]
    tag: []
author: buipy001gmail-com
metadata:
    author: buipy001gmail-com
#      description: Your page description goes here
#      keywords: HTML, CSS, XML, JavaScript
#      robots: noindex, nofollow
#      og:
#          title: The Rock
#          type: video.movie
#          url: http://www.imdb.com/title/tt0117500/
#          image: http://ia.media-imdb.com/images/rock.jpg
#  cache_enable: false
#  last_modified: true

---

With the change to the Joomla core coding to be consistent with the Model-View-Controller coding standard it allowed for Joomla to make use of template views that could be easily customised. This allowed for users to create HTML overrides for various parts of the Joomla output. It also meant that you did not have to modufy the core files of Joomla to customise the views. 

The concept of HTML overrides for Joomla isn't new. HTML overrides infact have been around since the release of [Joomla 1.5.0](http://www.joomla.org/announcements/release-news/4488-ladies-and-gentlemen.html "Joomla 1.5.0 release package") back on the 20th of January, 2008.

With the latest version of [Joomla 2.5.x](http://www.joomla.org/announcements/release-news/5403-joomla-250-released.html "Joomla 2.5.0 release notes") however, we did see the addition of being able to use and output multiple different views to modules within Joomla allowing a component or module to have assigned various different custom views throughout a website.

This article looks at implementing and creating a custom view for a module within Joomla.

We'll look at one of the core modules in Joomla 2.5.x that can have a template override created for it.

The method explained in this example tutorial can be applied to just about all components and modules in Joomla as long as they are created correctly.

You'll need to start by accessing the files that come with Joomla. Using a HTML editor like Dreamweaver will allowyou to explore the site structure of your Joomla installation.

Expand the modules folder from your Joomla install and then pick a module. In this example we'll be using the login module mod\_login.

 