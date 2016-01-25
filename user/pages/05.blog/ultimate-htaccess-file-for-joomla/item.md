---
# http://learn.getgrav.org/content/headers
title: Ultimate Htaccess File for Joomla
slug: ultimate-htaccess-file-for-joomla
# menu: Ultimate Htaccess File for Joomla
date: 15-04-2012
published: true
publish_date: 15-04-2012
# unpublish_date: 15-04-2012
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

For years I have been playing around with the main .htaccess file for Joomla and over time have created quite a beast of a file.

Not only does this .htaccess file provide the default search engine friendly URL functions as you'd expect with Joomla, it also applies a huge amount of security settings that can be applied in the .htaccess file as well as a set of optimisation and custom configuration settings to make your server work the way you want it to and now I'm going to share it with the Joomla community.

This blog post will go through in detail what each addition to the .htaccess file does allowing the user to understand and customise what they have in their own.

This file has been tested on many server configurations and many of our hosting partner servers and works quite nicely.

Please note that in some situations not all of these additions will work and will actually stop your site from work so please make a backup of your website and your original .htaccess file for restoration.

**Please make a backup of your website and .htaccess file before applying these changes.**

## ****Looking at the File

[Download the file (47kb txt)](wp-content/uploads/joomla-htaccess.txt "Ultimate Joomla htaccess file")

## Htaccess File Explaination and Credits

Only a few parts of the file are credited to myself, the rest has come from the Joomla community and the great people that have put together the resources for the HTML5 responsive boiler plate package.

Find out more at:

[http://docs.joomla.org/Htaccess\_examples\_(security)](http://docs.joomla.org/Htaccess_examples_(security))  
<http://html5boilerplate.com/>

 