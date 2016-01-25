---
# http://learn.getgrav.org/content/headers
title: Adding a Splash Page to Joomla
slug: adding-splash-page-joomla
# menu: Adding a Splash Page to Joomla
date: 16-04-2010
published: true
publish_date: 16-04-2010
# unpublish_date: 16-04-2010
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
    tag: [Joomla]
author: Peter Bui
metadata:
    author: Peter Bui
    description: Adding a splash page or a different home page to your Joomla website
    keywords: splash page, joomla
    robots: index, follow
#      og:
#          title: The Rock
#          type: video.movie
#          url: http://www.imdb.com/title/tt0117500/
#          image: http://ia.media-imdb.com/images/rock.jpg
#  cache_enable: false
#  last_modified: true

---

If you ever wanted create a slash page in Joomla you may have run in to the problem with the home button in your Joomla site's menu continually sending the users back to the splash page of a website. From a usability point of view, this can become very annoying for many users who are simply just trying to get back to the home page of the site. Here are some examples where we have solved this problem for the end user.

- [Angelakis Brothers](http://www.angelakis.com.au "link to Angelakis Brother's splash page")

There are a few ways to implement a splash page on to a Joomla site and this tutorial will take you through the process of one style of implementation.

When creating a splash page the file name is usually index.html. On most server configurations, the extension .html, will be higher in the order of file extensions to be loaded, hence will always loads before the main Joomla index.php file. The problem now arises when Joomla references the root level of the website in any navigation. It assumes that there isn't a splash page and it will lead to the user being redirected to the index.html file rather than the Joomla front page, index.php. The best way to get around this is to use the search engine friendly url settings in Joomla to create a new alias for the default Joomla index page.

1. Start by creating a new menu in the menu manager and call it Hidden. Specific details such as title, description and module title don't really matter as you most likely won't be touching this menu item again.
2. Next is to create a new **Menu Item Type**, choose Internal Link > Article > Front Page > Front Page Blog Layout. Set up the parameters to suit your front page layout and call it “home” and click save. At this point you will also need to set the menu item that you just created to the default for your site. Now anytime index.php is called, it will load this menu item that you have just created. This menu doesn't actually need to appear anywhere on the site layout. As its name states, it is a hidden menu.
3. Now, if you have an existing home button in your main menu site structure, check the alias for this home menu item. Make sure it is set as ‘home'. This will make sure that it's search engine friendly URL comes up as home.html. If you don't have a main menu item for the home button yet then create one in your main navigation on your site and like stated in the step above, set the alias to home.
4. Now the final step is to make sure that all the links on your site point to the home.html link. You'll most likely need to change this in these areas: 1. Splash page link to home.html
2. Logo links on your site
3. Any additional links in structure or navigation

If there are any more menu items that are linking to the home link, make sure that they are **Link Alias**, which is another menu item type, to your main menu home link.