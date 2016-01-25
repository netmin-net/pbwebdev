---
# http://learn.getgrav.org/content/headers
title: Joomla 1.6 Redirect Log and Anti Hack
slug: joomla-1-6-redirect-log-anti-hack
# menu: Joomla 1.6 Redirect Log and Anti Hack
date: 02-07-2011
published: true
publish_date: 02-07-2011
# unpublish_date: 02-07-2011
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

One area in Joomla 1.6 that I've written about awhile ago is the new Joomla Redirect component that comes with the new Joomla 1.6. Its a great little extension that picks up 404 errors and allows you to safely redirect them to the correct area in your website. It usually helps with search engine optimisation and also your web site users. Everyone hates landing on 404 pages.

Now, I have to admit that it has been a little while since I've looked at the redirect log on any of our Joomla 1.6 website but I just had a little peak into one a few minutes ago and noticed a huge list of automated hacking attempts! All coming from the same location over the course of a few days and then repeated attempts a few months later.

It wasn't a direct hack but it was obvious from the list that it was an automated script looking for particular components that might have been installed on the website to exploit.

What is the best thing to do in this situation?

1. Find the IP address of the referring website and blocking. Either blocking it with IP address with a .htaccess block, using a extension like RSFirewall or blocking the IP on your hosting environment using CSF (that should protect all yours sites on your server).
2. Have a look at some of your extensions and see if they're on the list. It might take a little bit of time but you'd need to figure out how potentially that component is being exploited. (Security vulnerability, spam attacks). It might be a good time to upgrade those extensions if possible.
3. Tell the Joomla community about the probe into your website and help others avoid being hacked.

Good luck securing your Joomla websites everyone and please let us know if you have other tips to block scripted attacks.