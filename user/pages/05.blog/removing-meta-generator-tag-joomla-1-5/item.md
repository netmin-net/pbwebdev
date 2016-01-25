---
# http://learn.getgrav.org/content/headers
title: Removing the Meta Generator tag from Joomla 1.5
slug: removing-meta-generator-tag-joomla-1-5
# menu: Removing the Meta Generator tag from Joomla 1.5
date: 13-09-2009
published: true
publish_date: 13-09-2009
# unpublish_date: 13-09-2009
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

Just recently I had to remove the default Joomla meta from the header of a few sites that we had made here. It is a very simple and easy step that can be done by anyone with a little HTML knowledge and not afraid to open up their main template files.

Navigate to the main index.php file of your template. Usually found under /templates/<name of your template> and open the index.php file with your favourite HTML editor.

Simply add in this line of code in the header of the file right at the very top.

<?php $this->setGenerator(”); ?>

We usually have a bunch of code her that removes alot of default Joomla stuff including the caption.js file and the main mootools.js files.

After that is done, simply upload the file and the <meta name=”Generator” content=”Joomla! – Copyright (C) 2005 – 2006 Open Source Matters. All rights reserved.” /> will be gone for good.

There are also other methods of removing the generator meta from the header of the site too but it involves modifying parts of the Joomla core. This was the old method that we use to use and found that it was over written in an update of Joomla a while back.

The file and code that you will need to modify for this method is called head.php

/libraries/**joomla**/document/html/renderer/head.php

you will want to find the following code (~line 167):  
 $strHtml .= $tab.'<meta name=”**generator**” content=”‘.$document->getGenerator().'” />'.$lnEnd;

you can turn it off by simply commenting the line with // at the beginning:  
 //$strHtml .= $tab.'<meta name=”generator” content=”‘.$document->getGenerator().'” />'.$lnEnd;