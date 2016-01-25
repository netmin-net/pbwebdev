---
# http://learn.getgrav.org/content/headers
title: Migrating K2 Items to Core Joomla Articles in Joomla 3
slug: migrating-k2-items-to-core-joomla-articles-in-joomla-3
# menu: Migrating K2 Items to Core Joomla Articles in Joomla 3
date: 23-07-2014
published: true
publish_date: 23-07-2014
# unpublish_date: 23-07-2014
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

![K2 items migration to Joomla 3 articles](/images/2014/07/k2-items-to-joomla-3-articles.jpg)

K2 is a great content construction kit (CCK) that makes it super easy to construct complex websites with complex content structures.

You can apply different templates to different categories and have some really interesting content displays, but for those that are using a very simple structure and don't need the extra bells and whistles that K2 provides, Joomla core articles is usually a really good fit and in most situations, users can do without the need of K2 altogether.

For some users, K2 is just too hard for them to grasp. The confusion between the Content menu and the Components->K2 menu is a usability issue if they haven't been overridden or replaced.

The idea of it was to give it extensive publishing features with a huge amount of flexibility but on the downside, the huge amount of flexibility can present users with so many options and parameters that they get overwhelmed and confused. In these sort of situations, Joomla articles is a better replacement, especially for small websites that more or less stay static for the existence.

A few of our clients fall into this category and we have created a migration script that pulls in K2 items and converts them into Joomla categories and articles.

The migration script is on our BitBucket server where you can access it and customise it for you projects.

[**K2 to Joomla 3 Articles migration tool**](https://bitbucket.org/pbwebdev/k2-joomla3-migrator/src/fe2767768862e9ab4a2285d0308d41290ad3ab07/?at=master)

This is a server PHP script that needs to be executed at command line in order for it to work. It is not a Joomla extension with a nice visual migration interface.

If there is interest in that perhaps we will build it but at the moment, you will need to be a competent developer to understand how to use it and migrate your content.

Please feel free to comment and improve the migrator, we'll be more than happy to provide assistance in regards to using it and helping you with your Joomla / K2 site migrations.

 

 