---
# http://learn.getgrav.org/content/headers
title: Breadcrumb Microdata Override
slug: breadcrumb-microdata-override
# menu: Breadcrumb Microdata Override
date: 22-07-2014
published: true
publish_date: 22-07-2014
# unpublish_date: 22-07-2014
# template: false
# theme: false
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration-status: review
    category: [Accessibility,Joomla,Search Engine Optimisation (SEO)]
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

There are some parts of Joomla's output that we believe can have extra microdata implemented directly into the core of the CMS but of course in some situations you may find that the build of the website doesn't need it, or doesn't want it, but in most, you should have it on by default.

[![Breadcrumb microdata example](/images/2014/07/breadcrumb-microdata-example.jpg)](/images/2014/07/breadcrumb-microdata-example.jpg)Breadcrumb microdata example



This HTML override that we use in the builds of our websites is what is required in regards to optimising your website and content to take advantage of the [breadcrumbs microdata schema](https://support.google.com/webmasters/answer/185417?hl=en "Breadcrumb microdata schema"). It is one of the easiest schemas to implement with about 4 lines of code that need to be added to the default breadcrumbs output to make it just that little bit better.

Adding in the microdata allows a user from a search engine results page be able to navigate to the other hierarchy levels of your website directly from the search engine results page. This helps when you have a deep hierarchy site with multiple levels. In the example that we show in this blog post, it does the page result for our Joomla training page which structurally sits under “What We Do” > “Joomla”. Having the right structure and breadcrumbs allows the user to jump back to the “Joomla” category level or the “What We Do” category level.

This post was a request at one of the Sydney Joomla User Group Meetups where we were talking about page and site optimisation and semantics of markup to get the best search results.

To install and use this override, download and unzip this file into your HTML overrides folder for your template.

/templates/<your\_template\_name>/html/

The default.php file should reside in the mod\_breadcrumbs folder.

/templates/<your\_template\_name>/html/mod\_breadcrumbs/default.php

**Download**: [mod\_breadcrumbs](/images/2014/07/mod_breadcrumbs.zip)