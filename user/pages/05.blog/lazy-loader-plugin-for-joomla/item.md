---
# http://learn.getgrav.org/content/headers
title: Lazy Loader Plugin for Joomla
slug: lazy-loader-plugin-for-joomla
# menu: Lazy Loader Plugin for Joomla
date: 22-04-2010
published: true
publish_date: 22-04-2010
# unpublish_date: 22-04-2010
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

![Lazy Loader for Joomla](/wp-content/uploads/2010/04/lazyLoader.png "lazyLoader")Built upon the jQuery library and the work done by [Mika Tuupola](http://www.appelsiini.net/projects/lazyload "link to Mika's lazy loader site"), this plug-in for Joomla loads images on long pages of a websites when the image appears in the users view pane. The idea and concept works is the exact opposite of [preloading images](http://www.appelsiini.net/2007/6/sequentially-preloading-images) before a web page loads. Lazy Loader actually loads images when needed.

This reduces bandwidth use and also server resources they are only called and downloaded when needed. Definitely a recommended plugin for large websites with long pages that are heavily image based, such as blogs or image galleries. An example of the plug-in in action can be seen at: [http://www.pbwebdev.com.au/blog/awe-inspiring-joomla-designed-websites](blog/awe-inspiring-joomla-designed-websites "example of Lazy Load")

## Installing and Configuring Lazy Loader for Joomla

Simply download the plug-in, install in the backend of Joomla, and enable it in the Plug-in Manager. The default settings should be the most compatible with most Joomla sites but further tweaking of the parameters may be required in order to get the plug-in to work correctly.

[![Parameters of Lazy Loader](/wp-content/uploads/2010/04/Screen-shot-2010-04-23-at-10.53.08-PM.png "Screen shot 2010-04-23 at 10.53.08 PM")](/wp-content/uploads/2010/04/Screen-shot-2010-04-23-at-10.53.08-PM.png)

## Definition of Parameters

**jQuery Library** This allows for the selection of different jQuery insertions to your site.

- Async: This uses the asynchronous calling method to dynamically load the compressed jQuery library
- Static: This calls the compressed jQuery library via a static URL
- Disable: Disables the insertion. Good when the library is already called by another extension.

**Threshold** This refers to the amount of pixels away from the images and the “screen fold” to start loading the image. Default is “0”.

**Placeholder** This is the default image that is used as the place holder before the real image is loaded. Default is: “/plugins/system/lazyloader/grey.png”

**Effect** Refers to the type of image load effects apply. At the moment there is only appear and fade in. In later releases we'll implement more image effects.

**Event** This will load the images on different events. Events available are Scroll (default), on mouse over and on mouse click.

**Container** The container refers to a specific div container that you might want the lazy loader to apply to only.

**Failure Limit** This will limit the amount of image searches done by the plug-in before ending itself when there are errors. Default is 10.

## Known Issues

There are some conflicts with other modules and components. FrontPage Slide Show by JoomlaWork and some YooTheme Javascript enabled modules. In later releases we'll be improving the compatibility and also a Mootools version to work without jQuery in Joomla.

## Version Notes

Version 1.1 – 23rd April 2010

- Included new animation effects, slideUp, SlideDown
- Cleaned up presentation of plugin parameters

Version 1.0 – 22nd April 2010

- Released

## Next Version

- Mootools integration
- Lots of bug fixes. LOTS

## About jQuery and its LazyLoader Plugin by Mika Tuupola

If you'd like to learn more about the original jQuery plug-in please refer to Mika's site and documentation: <http://www.appelsiini.net/projects/lazyload> <a name="download"></a>

## Download the Plug-In

- **Download the plug-in: [plg\_lazyLoader-1.1](/wp-content/uploads/2010/04/plg_lazyLoader-1.1.zip) (7.2kb)**

** **