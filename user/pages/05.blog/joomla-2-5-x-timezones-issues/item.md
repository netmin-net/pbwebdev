---
# http://learn.getgrav.org/content/headers
title: Joomla 2.5.x Timezones Issues
slug: joomla-2-5-x-timezones-issues
# menu: Joomla 2.5.x Timezones Issues
date: 20-11-2012
published: true
publish_date: 20-11-2012
# unpublish_date: 20-11-2012
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
    tag: [Joomla,Joomla]
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

![timezones in Joomla](wp-content/uploads/2012/11/time-zones.jpg)We noticed the other day that a few new Joomla users that were playing around with the later series of Joomla 2.5.0-2.5.7 (onwards) were having issues with the timestamp and timezones that were set up in their websites.

This is a pretty common problem if you don't have the right setup on your server so lets look a little deeper into what is going on.

## Specific Issue with Joomla 2.5.4 and Timezones

There is however another issue with the timezones if you are running Joomla version 2.5.4. If you are running this version and you are running PHP 5.3.x then you may need to also upgrade your version of Joomla to the latest version which will also patch the issue within the timezone files in Joomla.

The issue can be found and tracked on: [http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker\_item\_id=28535](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=28535)

Within the issue threads we can also see the patches required to fix the issue specificlly for Joomla 2.5.4: <https://github.com/joomla/joomla-platform/pull/1293>

The easiest way to fix the issue is to upgrade to the latest version of Joomla 2.5.x series.

## Fixing the Issue of Timezones in Joomla 2.5.x

If the problem presists, try upgrading the version of PHP that you are using.

If you're running one of the later version of Joomla, that is Joomla 1.6 onwards, you may need to make sure that your web hosting environment is using PHP 5.3.x. At the time of writing this article the latest stable version of PHP is 5.3.18 and PHP 5.4 is already being used in some environments. Staying on PHP 5.2.x is actually a security risk and it is highly advisable to upgrade as the series of PHP became end of life and was no longer supported for quite a while.

We can see from the forum post mentioned earlier that there is [one user](http://forum.joomla.org/viewtopic.php?f=615&t=709784#p2805911) that has a web server that is running PHP 5.3 and has the timezones working perfectly.

Web hosts should not be charging to upgrade the server environment. On another note, when upgrading the server environment, make sure that everything that is running on the server will work with PHP 5.3 as some sites or extensions may break!