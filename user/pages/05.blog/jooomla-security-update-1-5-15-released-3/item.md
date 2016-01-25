---
# http://learn.getgrav.org/content/headers
title: Jooomla Security Update 1.5.15 Released
slug: jooomla-security-update-1-5-15-released-3
# menu: Jooomla Security Update 1.5.15 Released
date: 06-11-2009
published: true
publish_date: 06-11-2009
# unpublish_date: 06-11-2009
# template: false
# theme: false
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration-status: review
    category: [Joomla,Security]
    tag: [Joomla,Updates,Website Security,Joomla,Updates,Website Security]
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

## What does this patch cover and why you should upgrade.

The patch blocks two security vulnerabilities that are found in Joomla. They aren't ones that I have come across before or have seen sites hacked as a result of it but since the vulnerabilities have been identified it is fairly important to upgrade and patch the holes up.

### Security Patch 1

***When logged into the front end with Author access, it was possible to replace an article written by another user.***

The majority of the sites that we build have front end editing disabled and only back end editing is allowed. If this is not the case then please make sure that you contact us to make sure this security patch is applied to your site.

### Security Patch 2

***It is possible to read the contents of an extension's XML file and find the version number of the installed extension. This could allow people to exploit a known security flaws for a specific version of an extension.***

These XML files contain the installation information of any templates, component,module or plugin of any addon or even any extension that is shipped out with Joomla. If a hacker knows of a version of a extension that has a security flaw, then they could potentially crawl the net for Joomla sites that use this particular extension and take advantage of the security hole.

This is an important update especially if you use a lot of third party extensions and you don't know how well they are written. Personally I don't think it is a likely possibility if your Joomla site is locked down in terms of security but it can happen.

Please [contact us](http://www.pbwebdev.com.au/contact-us.html "Contact PB Web Development") and let us know that you would like your Joomla site upgraded. It is a straight forward process and well worth doing.

**What else came out with the patch?**

- TinyMCE is now working properly – all remaining bugs created by the recent TinyMCE upgrade should be gone now
- Mootols were upgraded to 1.12 to ensure future compatibility with Firefox 3.6
- PHP 5.3.x compatibility – Joomla runs fine on PHP 5.3.x now (except of OpenID library)