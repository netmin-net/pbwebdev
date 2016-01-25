---
# http://learn.getgrav.org/content/headers
title: K2 2.6 Upgrade Issue: Model class cpanelModelCpanel not found
slug: k2-2-6-upgrade-issue-model-class-cpanelmodelcpanel
# menu: K2 2.6 Upgrade Issue: Model class cpanelModelCpanel not found
date: 09-10-2012
published: true
publish_date: 09-10-2012
# unpublish_date: 09-10-2012
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

\*Please note: New update to K2 2.6.1 will fix the issue. Make sure you read the update notes as there are changes to the login/user module and overrides for it.  
  
 K2 v2.6.1 now available <http://t.co/KUe27lNY> Fixes minor bugs (notices & CSS related), includes 2 very important changes! Overrides updated!

We were pretty excited to see the latest version of K2 to come out with compatibility with Joomla 3.0. There was just one minor bug that we found when installing it on a Joomla 2.5.7 website.

The latest release of the content construction kit from K2 came just one little bug that we've noticed in the upgrade process.

**Model class cpanelModelCpanel not found**

This particular error can be found on the control panel after an upgrade of K2 to the latest version 2.6.0. The upgrade method used was the default extension upgrader found in the core of Joomla rather than downloading the new extension from the GetK2.org website.

![Screenshot of Cpanel error after upgrading to K2 2.6](wp-content/uploads/2012/10/k2-26-error.png)

This one is an easy fix.

 

To fix the issue, simple navigate into the file structure of your Joomla site via FTP or a web hosting control panel.

Go to** /administrator/components/com\_k2/models**

Locate the file “**cpanel.php**” and remove or rename the file.

This is an old legacy file that is used in the older versions of K2 and can be removed safely if you're moving forward with the latest version of K2.

Please make sure you backup your website before making any changes on your website.