---
# http://learn.getgrav.org/content/headers
title: Removing mootools-core.js and caption.js from Joomla
slug: removing-mootools-core-js-caption-js-joomla
# menu: Removing mootools-core.js and caption.js from Joomla
date: 03-06-2011
published: true
publish_date: 03-06-2011
# unpublish_date: 03-06-2011
# template: false
# theme: false
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration-status: review
    category: [PB Web Dev]
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

When I build a site I want to remove any unneeded external JavaScript files in the html to help improve the performance of the site.

So when I create a basic content page using an article layout with no modules I am surprised to see these 3 lines

<code>

 
    <script src="/media/system/js/core.js" type="text/javascript"></script>
    <script src="/media/system/js/mootools-core.js" type="text/javascript"></script>
    <script src="/media/system/js/caption.js" type="text/javascript"></script>

</code>

This happens on both joomla 1.5 and 1.6 When I looked around the web for a solution I keep finding the answer to be use regular expression on the final output to remove it. While this will remove it, I wanted to understand why this is added. It should in theory only be added when it is needed. If I add a module that does need mootools then I do not want to be removing the script file.

It will break the module. Not being a core hack is probably the only good thing about this method. Since Joomla will only add files that are told to be included, so I decided to work out why they were being told to be included when nothing on the page needs them.

## The Reason

Digging in to why, this is what I found: In the com\_content component it is calling

<code>

 
    JHtml::_('behavior.caption');

</code>

This one line is causing those 3 JavaScript files to be added to the page It is either an overlooked bug, or removing it causes other bugs to be visible.

## How to fix

All you need to do is comment out a line in a core component com\_content. <b>This is a core hack</b> any update will revert this change and you will have to manually update it. ok on to the fix.

In the file: “/components/com\_content/controller.php” find: “public function display($cachable = false, $urlparams = false)”   we just comment out:

<code>

 
    JHtml::_('behavior.caption');

</code>

so it will become

<code>

 
    //JHtml::_('behavior.caption');

</code>

Thats it!

## What Next

Add a comment below if this worked for you or you had any problems implementing this hack.