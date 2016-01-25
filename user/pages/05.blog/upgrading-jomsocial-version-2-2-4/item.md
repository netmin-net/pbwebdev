---
# http://learn.getgrav.org/content/headers
title: Upgrading JomSocial to Version 2.2.4
slug: upgrading-jomsocial-version-2-2-4
# menu: Upgrading JomSocial to Version 2.2.4
date: 13-10-2011
published: true
publish_date: 13-10-2011
# unpublish_date: 13-10-2011
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
    tag: [Joomla,Social Media,Joomla,Social Media]
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

[![JomSocial 500 Error](wp-content/uploads/2011/10/Screen-shot-2011-10-13-at-4.34.46-PM-150x150.png "JomSocial 500 Error")](wp-content/uploads/2011/10/Screen-shot-2011-10-13-at-4.34.46-PM.png)JomSocial is a fantastic community component for Joomla. It allows for social interaction between members of a website with similar features like Facebook.

Recently we went through an upgrade process for a client website, CanverVoices.org.au but ran in to an error after the upgrade.

500 \*\*\*\*\* /components/com\_community/events/wall.trigger.php:26

Definitely something you don't want to see after upgrading.

After crawling the web to see if there was a viable solution, one did come up to simply comment out the line from the file which is an easy enough fix until it can be investigated further.

Navigate to: **/components/com\_community/events/**

Within the file structure of your website and look for the file called **wall.trigger.php**.

On line 26 of this file you will find this:

 
    		CError::assert( $row->comment, ', '!empty', __FILE__ , __LINE__ );

 

This line of code appear to handel some sort of error code and message that may appear on the website. In this case we're just going to comments out this line of code with **// . **Your new line of code should look like this.

 
    		// CError::assert( $row->comment, ', '!empty', __FILE__ , __LINE__ );

 

A simple enough fix until you or the JomSocial team can investigate further to find out what the real problem is.