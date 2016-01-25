---
# http://learn.getgrav.org/content/headers
title: Sydney Joomla User Group &#8211; Upgrading Joomla 1.5->1.6+
slug: sydney-joomla-user-group-upgrading-joomla-1-5-1-6
# menu: Sydney Joomla User Group &#8211; Upgrading Joomla 1.5->1.6+
date: 24-04-2012
published: true
publish_date: 24-04-2012
# unpublish_date: 24-04-2012
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
    tag: [Updates,Updates]
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

This month in April we looked at upgrading Joomla using SP Update or JUpgrade for Joomla. Both methods have its pros and cons as we looked deeper into how they work.

The part that I presented on was the SP Update method using the component from [CyEnd](http://cyend.com/extensions/extensions/components/5-upgrade-joomla-from-15-to-16 "Cyend SP Upgrade for Joomla 1.5").

**[Joomla upgrades](http://www.slideshare.net/peterbui1/joomla-upgrades "Joomla upgrades")**

View more presentations from [Peter Bui](http://www.slideshare.net/peterbui1)

 

## SP Udate Overview

The component overall does a good job of updating and migrating data from Joomla 1.5 to 2.5.x series.

My personal opinion of the component is that it will get the job done but there is still more work to do afterwards to help fine tune the process of upgrading the content to the website. As with any automated processes there is always more work to do.

With upgrading our own websites from Joomla 1.5 -> 2.5.x we've found it easier to copy the data from the tables over manually and setup default permission levels and category assignment for all the entires and then manually reassigning or rearchitecturing the website.

This is a step that we usually would have done either way with upgrading a website and more likely prefered method internally at PB Web Development.

For other custom databases or components that SP Upgrade didn't update, you'll have to manually rebuild or update these as well to suit Joomla 2.5.x.

At least the upgrade path to Joomla 3.0.x will be much easier.