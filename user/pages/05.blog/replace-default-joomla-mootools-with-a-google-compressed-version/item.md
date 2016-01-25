---
# http://learn.getgrav.org/content/headers
title: Replace Default Joomla Mootools with Compressed Version
slug: replace-default-joomla-mootools-with-a-google-compressed-version
# menu: Replace Default Joomla Mootools with Compressed Version
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
    tag: [Joomla,Server,Joomla,Server]
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

There are some minor benefits in replacing the default Mootools library with a compressed version called from a Google server. The main advantages being that the file is highly compresses from the original 73kb to a tiny 18kb. Secondly the response time from the Google server is much higher than our own web hosting environment. Perhaps we should upgrade? Lastly, the final advantage is that this file may already be cached in the user's browser from another website meaning that it won't have to be downloaded at all, saving another 18kb. Fantastic!

One disadvantage is that your site will have to make one more DNS call t a different domain which will add to the load time of your website but this disadvantage is definitely outweighs by the gains of the compresses and hopefully cached copy from the Google server.

So how do I go about implementing this fancy new speed increase.

Located your template file within Joomla. (These screen shots that we are providing are from the JA Purity template that comes with Joomla). The easiest way to edit the template files is through the template manager under Extensions in the administrator area of your site.

Include this little bit of code at in the top declaration part of the template. Just at the end before the closing php tag ” ?> ”

 
    $document =&JFactory::getDocument();
    unset($document->_scripts[$this->baseurl . '/media/system/js/mootools.js']);

[![Screen shot 2010-04-10 at 10.14.27 AM](wp-content/uploads/2009/09/Screen-shot-2010-04-10-at-10.14.27-AM.png "Screen shot 2010-04-10 at 10.14.27 AM")](wp-content/uploads/2009/09/Screen-shot-2010-04-10-at-10.14.27-AM.png)

Now scroll down a little further in the file and add in the code required to call the Mootools file from the Google AJAX library.

 
    <script type="text/javascript" src="http://www.google.com/jsapi"></script>
    <script type="text/javascript">google.load("mootools", "1.1.2");</script>
    
    <a class="grouped_elements" href="wp-content/uploads/2009/09/Screen-shot-2010-04-10-at-10.21.54-AM.png" rel="tc-fancybox-group" title=""><img alt="Screen shot 2010-04-10 at 10.21.54 AM" class="aligncenter size-full wp-image-318" height="112" src="wp-content/uploads/2009/09/Screen-shot-2010-04-10-at-10.21.54-AM.png" title="Screen shot 2010-04-10 at 10.21.54 AM" width="456"></img></a>

This uses the loading method as define at the Google AJAX Libraries API

<http://code.google.com/apis/ajaxlibs/documentation/index.html#mootools>

If that doesn't work for you, you can call the file directly by pasting in:

 
    <script type="text/javascript"
    scr="http://ajax.googleapis.com/ajax/libs/mootools/1.1.2/mootools-yui-compressed.js">
    </script>

You should now have a slightly faster loading website. Use tools such as [YSlow](http://developer.yahoo.com/yslow/ "Yahoo Developers YSlow") and [Google Page Speed](http://code.google.com/speed/page-speed/ "Google Page Speed") to do some testing to find out how much your site actually decreased in load time.

This post is an adaptation of methods from:

- http://hut32.blogspot.com/2009/04/how-to-remove-inclusion-of-mootools.html
- http://blog.joomlaworks.gr/replace-mootools-in-joomla-with-a-compressed