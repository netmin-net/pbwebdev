---
# http://learn.getgrav.org/content/headers
title: Website Launch Check List
slug: website-launch-check-list
# menu: Website Launch Check List
date: 14-04-2015
published: true
publish_date: 14-04-2015
# unpublish_date: 14-04-2015
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

There is a huge list of things to check when launching a website and here is a good checklist that we follow in regards to launching a website.

If you have any recommendations or additions, please feel free to add in the comments and have them contributed to the list.

## Pre Launch

### **User Acceptance Testing**

Check list against all the functional specifications that have been defined for the project

User Acceptance Testing is a beast of a check in its own right. Depending on the website and what the requirements are you will need to write the various tests that will need to pass in order to launch the website.

Do people need to register on the website? Does a user need to be able to use a contact form?

These tests should be define at the stages of building so that a developer or site builder has something to build against for testing.

Here is a list of a few generic functions that should be testing on all websites:

- Search function
- Login function
- Registration
- Contact form

peter@gmail.com

peter+fdsa@gmail.com **Jack**

mail mailinator send anything to this address, **Hardy**

Additional development tools like Behat can help with automated test script writing to ensure that your website and code is always working and is always tested against a standard test.

### **Website Content and Style Audit**

At this stage you should be looking and checking to make sure that all of the fonts, typography, images and content is all right across the site.

Everything from correct image size and optimisation, to spelling errors and typos throughout the site.

- Typography
- Styles
- Content
- Menus
- Broken links

### Browser Testing

This should go hand in hand with the actual development of your theme or template.

A great tool to help browser testing is BrowserStack. It will allow you to emulate many different types of browsers and different operating systems to help make testing on different environments just that much easier.

Make sure that your site is working on all required browsers as specified in your build specifications.

We like to support all modern browsers such as the latest version of Firefox, Chrome and Safari as well as backdating our support on Internet Explorer to IE9 as this works nicely with Bootstrap 3 which forms the foundations of many of our templates.

http://www.my-debugbar.com/wiki/IETester/HomePage

 

### Hosting Check

This is something you might want to do well in advanced of launching. Check to see if the web server that you are going to launch the website on is up to scratch and is ready to work with your website. A lot of hosting companies still aren't using the latest versions of PHP and for a CMS like Joomla, an old version of PHP will not work since it has a minimum PHP requirement of 5.3.10.

Test and make sure you can deploy to the server and get your website working well before the launch date.

There is nothing worse than going to launch a website with something like AkeebaBackup assuming that everything will be ok and coming into issue after issue with the server on launch.

Check legals behind the hosting, hosting overseas may have complications.

### Site Speed Optimisation

Site speed is critical. You will need to make sure that your website is loading fast and is loading well. Google uses site speed as a contributing factor for rankings and a slow performing website will mean a potentially impacted site ranking.

Using tools such as Pingdom Tools and Google Page Speed will help you benchmark the site speed and give you some guidance in regards to where and what to update and upgrade on your site.

We like to use third party Joomla extensions to help optimise our websites.

- T3 framework, as it comes with CSS and JS compression that works nicely
- MaxCDN, allows us to quickly and easily create a website on a content delivery network
- jFinalizer and JCHOptimise, these two tools allow use to compress assets and various parts of the website even further.
- Caching turned on
- Dev mode in template engines turned off
- Server caching if available, turned on
- Apache and NGinx can do compression on the fly (jack)

### Global Configuration Settings

A few other things to check in your Joomla site include a few settings in your Global configuration

- Error reporting set to none
- GZip compression is turned on
- Time zone set correctly
- FTP details are not set
- Site name and settings and configured properly not using personal details or emails
- SMTP, Mandril Sendgrid

 

### E-Mail

Setup your clients with Google Apps or a third party email provider. Makes your life easier.

 

## Post Launch

When you've launched your website and you have made it visible to the world on the production server, there is another great list of things to do to ensure the best possible outcomes.

### Search Engine Optimisation

To make sure that your site is seen and is being index be the search engines, we have to make sure that the site is properly setup for them.

Here are a few things to do to make sure that you're ready

- Search Engine Friendly URLs are turned on and set up properly in your Global Configuration (check the permission on the file to make sure it works, Hardy)
- Install and configure Google Analytics
- Link up with Google Webmaster Tools
- Create an XML sitemap and submit it to Google Webmaster Tools, xml-sitemaps.com (hardy) MijoSEF, OSMap
- Bing search submission (actually haven't done this in years)
- Enable conversion tracking if you're running Google Adwords or if you are running an eCommerce store
- Modify your robots.txt file to suit your website.

### Security

Is the launched website up to date and are the extensions that it is using up to date?

If not, why not. Every extension and version that you are out of date is potentially another security hole or vulnerability that you may be opening up your website to. Make sure that you're launching an up to date website.

Use nice security tools like **AdminTools** to help you to lock down the security of your website and keep it that much more secure.

A third party tool that can help you with your security is **MyJoomla**. MyJoomla provides a great security audit and management service where it will scan your website for malicious code or possibly hacked code on your site. It isn't easy to use and understand at first but a hugely helpful and useful tool once you know and understand how to use it.

### Management

Managing your website in the long term can become tedious and time consuming. In fact, if you have hundreds of websites that you are managing and updating, it can take hours, if not days to update them all when security alerts, patches and new releases are produced.

Using a management tool like **Watchful.li** will allow you to manage multiple websites from one console. You will be able to update, backup and manage them all from one centralised location without the need to login to all of them one at a time and updating them one at a time.

This is where making sure you're following good Joomla! development practises so that you can manage your website in this way.

Additional tools such as **Pingdom** may come in handy to track website uptime.

### Social Media

The importance of social media for any website and business these days is critical. So many more people go by recommendations from their friends and networks more than anything else.

After launch, make sure all of your social media accounts for the website are connected, setup correctly and is working for the website. If you're auto posting to social networks from the website, make sure they work and there is a process in place to reset them in case a connection expires.