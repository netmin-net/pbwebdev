---
# http://learn.getgrav.org/content/headers
title: Drupal Invades Joomla Territory
slug: drupal-invades-joomla-territory
# menu: Drupal Invades Joomla Territory
date: 12-04-2011
published: true
publish_date: 12-04-2011
# unpublish_date: 12-04-2011
# template: false
# theme: false
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration-status: review
    category: [Drupal]
    tag: [Drupal,Drupal]
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

![drupal-invades-joomla](wp-content/uploads/2011/04/drupal-invades-joomla.png "drupal-invades-joomla")At the Sydney Joomla User Group Meeting this April we see [Ryan Cross](http://www.ryancross.com "Ryan Cross Drupal Developer") giving the group a presentation on Drupal. Ryan's presentation really has given the SJUG a look into Drupal and how it differs from Joomla. Ryan's presentation looked at some of the new features on Drupal 7 as well as setting up content types and packaging up code to push out to production servers. See our [Facebook fan page](http://www.facebook.com/album.php?aid=346154&id=152767770861&l=1cb7c46a3e "Sydney Joomla User Group Meeting April") for pictures from the night.

Below are some of the notes that I had taken on the night. Mostly for our own reference but I'm sure other members of the Sydney Joomla User Group may find it interesting.

### Some Benefits of Drupal

Drupal has a fairly large security team checking everything in the core and even the contributor modules that extend Drupal. There are also automatatic testing of these modules that push code through over 40,000 (might have been 4000) different tests to see if patches and work. It is a fantastic and fast way to review code that gets pushed out for Drupal. Package code to deploy is also another useful feature as well as the standard content construction kits and taxonomy that is built into Drupal. There is also lots of local support for Drupal users in Australia and can all be found on the Drupal groups website.

### Some Interesting Information About Drupal

Roughly 2% of the world's websites use Drupal compared to 2.7% for Joomla. A few high profile websites that use Drupal include:

- [whitehouse.gov](http://www.whitehouse.gov/ "Whitehouse.gov")
- [Tarongazoo.com.au](http://www.tarongazoo.com.au "Taronga Zoo")
- [pm.gov.au](http://www.pm.gov.au/ "Prime Minister")
- and even CiviCRM started off on Drupal.

Drupal is also used to been drive iphone apps, Facebook apps and desktop clients applications. Drupal sites behind all of these front facing applications and pushes data out to the applications via the web interface. On installation of a Drupal website, preconfigured packages can be used to quickly deploy a website as a e-commerce website, social networking, or even an Intranet. There a lots of preconfigured packages available for website deployment. When installing Drupal without a predefined package, you'd find the installation very bare with no editors or ‘extras' within the installation. Drupal 7 has a few new features in it that are vast improvements from the older versions of Drupal. A lot of money has been spent on the usability of the system allowing for easier use of the system.

Permissions on Drupal are very gradual, with lots of options in configuring the permissions for who has access to what. Very easy to setup modules to control what users see. The Drupal Blocks is very similar to modules in Joomla or widgets in WordPress.

Themes define the regions in which the site and blocks are then assigned. Assigning the blocks into the site is as simple as dragging and dropping block types into these predefined regions. Contextual configuration allows an administrator to control how the block and when the blocks are displayed. There features are all very similar to Joomla. Only difference is Joomla allows for simple point and click controls and options rather than simply adding them in contextually. Multisite within Drupal is possible via, domain access.

Single code base can run multiple websites outside of the main site. Websites can share table or only shared parts of a table such as the users and sessions tables and not the roles table, allowing for multiple site access without need to login.

Multiple databases with master and slave databases are also possible. Slave databases can be read only and and master database can be both read and write allowing for maximum configuration. Druapl 7 also has the ability to interfaces straight into Flickr and YouTube and content storage. Users won't even see the YouTube or Flickr interfaces as they use the website.

### My General Conclusions

From Ryan's presentation on Drupal 7, I've personally can see it being very similar to Joomla in some ways. I likened it to Joomla 1.6 + K2 + Sobi2 but all packaged into on release and very well refined. For anyone want just a simple straight forward implementation then WordPress of Joomla might be the best solution but in the case of complex functionality, Drupal would be the better choice.

### What CMS is Better? WordPress, Joomla or Drupal

In saying which CMS/platform is better, I have to say it is a case by case scenario where using the right tools for the job is the best approach. If you were to build a very simple straight forward brochure style website, I'd recommend WordPress.

Especially if the client or website administrator has limited computer skills. The administrator interface for WordPress has to be one of the most friendliest with all most everything being a few clicks away. Joomla would be a better options where WordPress's functionality and flexibility falls through. If a suitable WordPress solution can't be found then using Joomla might be the easier option.

I the case where lots of customisation is needed with websites containing different content profiles, access control and complex site taxonomy then Drupal might be the best option there.

\* The notes below this point have not been edited \*

Feature update to push code out to a new production website rather than working off live.

Most admins accounts on a live site. Coupled with version control can become very powerful way of publishing to a live website.

Remember to install drush and run it in the terminal Content translation server, delivering new languages for the interfaces from the main Drupal repository.

Localization corrections can be pushed to a repository of main server.

 