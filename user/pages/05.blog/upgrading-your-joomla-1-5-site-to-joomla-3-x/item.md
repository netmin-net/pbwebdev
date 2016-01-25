---
# http://learn.getgrav.org/content/headers
title: Upgrading Your Joomla! 1.5 Site to Joomla! 3.x
slug: upgrading-your-joomla-1-5-site-to-joomla-3-x
# menu: Upgrading Your Joomla! 1.5 Site to Joomla! 3.x
date: 13-07-2014
published: true
publish_date: 13-07-2014
# unpublish_date: 13-07-2014
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

[![joomla15-upgrade-migrate-joomla3](/images/2014/07/joomla15-upgrade-migrate-joomla3.jpg)](/images/2014/07/joomla15-upgrade-migrate-joomla3.jpg)

One of the biggest issues with many Joomla! sites still on Joomla 1.5 is the upgrade path from Joomla 1.5 to Joomla 3.x. We have found a lot of customers and potential customers that are resistant to the upgrade as it is costly, time consuming, hard to do and isn't worth their time and investment.

This article goes through a little **history** of the process, **why** it is worth upgrading from Joomla 1.5, why it is the **perfect time** to do it now and **how easy it really is to start** the process and migrate to the latest version of Joomla.

In the early days of the Joomla 1.6, 1.7 and 2.x releases we saw a lot of resistance and difficulties in regards to upgrading to the latest version of Joomla. There are of course tools that came out a little later that helped with the process but if you were not a developer or understood what you were doing, it wasn't an easy process.

For a lot of small businesses, bloggers or small agencies that were managing Joomla 1.5.x websites this meant a huge operating cost in regards to upgrading the websites in order to maintain security and functionality.

A lot of these websites were left on Joomla 1.5 or migrating to another Content Management System (CMS) that seemed a little easier to upgrade to and maintain.

Joomla isn't the only CMS that is like this. Drupal is also a CMS that has no clear migration path from one release to another and in fact can incur huge costs in regards to upgrades and maintenance from one version to another.

## Why Upgrade

**What is the point of upgrading and what are the benefits?**

The point of upgrading to a different version is to take advantage of new features that are in the later releases. New features, security, better coding standards and much more can be found in the latest release of Joomla making it one of the best releases ever.

New features such as:

- Integrated micro data schemas makes Joomla websites search results relevant and in context with what a user might be searching for.
- New security features such as Bcrypt password encryption makes it extremely difficult to brute force hack a username and password combination.
- Two factor authentication which enables to a secondary physical password that is dynamically generated from a device such as a mobile application or Yubikey forces bank and financial institute level of security.
- Tagging system allows for more dynamic content discovery and more flexible categorisation of content in a website
- Versioning allows for roll back and comparison of different content that is saved in the site
- Integrated Bootstrap framework meaning that all Joomla sites from a default installation are completely mobile ready and fully 100% responsive.
- Complete access level control with unlimited levels of access and granular control means you can create a complex website with unlimited levels of access and permissions
- Full translation and multilingual capabilities means you can tap into other language speaking countries such as Chinese (14.4% of the world population) and Spanish (6.5% of the world population). Both of these languages are spoken by more people in the world than there are native English speaking people (5.43% of the world population). Translating your website into the top three speaking languages in the world will reach potentially 26.3% of the world's population and it can be easily done with Joomla.

These are just a few of the features and capabilities of Joomla out of the box and if your business wants to take advantage of these opportunities then Joomla is the perfect CMS solution and the perfect reason to upgrade.

The other main reason to upgrade is for security itself. Every minor and major release of Joomla not only comes with more features but also comes with security patches and security improvements. Making sure that your Joomla website is up to date on the latest versions will ensure that your website and online asset is protected from hackers and security exploits.

Not upgrading to protect your website could cost you more time and money than not doing it at all.

## Perfect Time to Upgrade

**Why is it a perfect time to upgrade to Joomla 3.x now?**

Over the past year the Joomla project, from our point of view, has matured. Not only in the code and the CMS but also the community of designers and developers that are behind all of the code. Changes to the release life cycle, the ability for anyone with no technical knowledge to test releases and patches and much more have improved so many aspects of the project.

### The Upgrading Tools

The very tools that are used to upgrade a Joomla 1.5 site to Joomla 3.x are all very well used and supported by the developers that make them and the community that use them.

Tools such as [JUpgradePro](http://extensions.joomla.org/extensions/migration-a-conversion/joomla-migration/23338 "jUpgradePro on the Extension Directory"), [SPUpgrade](http://extensions.joomla.org/extensions/migration-a-conversion/joomla-migration/15609 "SP Upgrade on the JED"), [Migrate Me Plus](http://extensions.joomla.org/extensions/migration-a-conversion/joomla-migration/24238), [Ji Migrator](http://extensions.joomla.org/extensions/migration-a-conversion/joomla-migration/23591), and r[edMigrator](http://redcomponent.com/redcomponent/redmigrator) are all well supported and documented migration extensions that make the process from Joomla 1.5 to Joomla 3 very easy. Install the required components, click a few buttons on the Joomla 1.5 and the Joomla 3 versions of your website and the data, user tables and content will be migrated over for you!

Our personal preference in upgrade tools at the moment is **JUpgradePro** followed by **Ji Migrator**. These are the two easiest to use migration tools that we have come across lately.

### Stable Release of Joomla 3.x

Joomla 3.3.1, which is the stable release of Joomla at the time of writing this article has been tested over and over and is one of the most tested versions of the CMS ever. A lot of people were waiting for version 3.5, which is seen as a long term support and stable version but that now has changed. The versioning of Joomla is now a more semantic and structured versioning with no fixed numbers being a ‘stable' release. All versions of Joomla are stable releases and should be the one that you're using.

## How to Start Upgrading

So now you know all of the reasons why and when you should upgrade your site to the latest version of Joomla how do you start the process?

### Pick Your Tool

Start by looking at the migration tools that are out there with our pick being JUpgradePro as a start.

### Start the Data Migration

It is free and very well documented in regards to the process of upgrading a website. Download the JUpgrade extension, install on to your Joomla 1.5 and new Joomla 3.x website and choose the parts that you want to migrate.

If your site has more extensions such as K2, Flexicontent, Kunena etc, there are [paid extra plugins](http://matware.com.ar/jupgradepro-3rd-extensions-plugins/level.html) that you can install to continue the process and make it as easy as possible to upgrade your website with a few clicks.

### Migrate the Template or Install a New Look and Feel

Once all of the data and information is upgraded, you will have to look at the template of the website. Usually the template from Joomla 1.5 to Joomla 2.5 and Joomla 3 will differ slightly. This is the perfect opportunity to look at a redesign of the website and also to look at a mobile and responsive template to give your customers and readers of your website the best mobile experience.

### Test, Test and Test

Now that you have migrated all of the data and have a new look and feel to the website, it is time to test the site. There are a few things that are critical and you must test in order to get things right.

**Test the navigation**: Since they've all been recreated, you will want to make sure that all of the links in the menus across the website are working correctly.

**Functionality test**: Make sure all of those website functions are working from front end logins, sign ups and search forms. It may all look right but make sure that all the functions are actually working and not just looking pretty.

**Search engine results**: This is critical! The search friendly URLs from a Joomla 1.5 to any other version of Joomla may have changed and it is important to set up 301 redirect on your website to ensure that all of the URLs that Google has indexed are all going to the right places and where they should. Not doing so can result in your website not appearing in Google after your upgrade.

## Need Help?

If it all seems too overwhelming or you find that your time is better spent elsewhere such as selling your services, products and in areas of business development for yourself, then contact the team at PB Web Development to help you with the migration process of your Joomla 1.5 website to the latest version of Joomla.

### **Sign up to learn more about upgrading your Joomla website for free**

 Your email address     Subscribe

 The hours that you could be spending working out how to start could be better spent going fishing, scrolling through Facebook or liking cat photos on Instagram. Let us do all the hard work of the migration and care of your website.

You can email us, [mail@pbwebdev.com.au](mailto:mail@pbwebdev.com.au) or call [(02) 9357 4420](tel:+61 2 9357 4420) to find out more about how we can help you with a Joomla 1.5 Upgrade and migration to the latest version of Joomla.

 