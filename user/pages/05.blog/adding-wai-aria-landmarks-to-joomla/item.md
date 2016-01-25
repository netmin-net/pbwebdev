---
# http://learn.getgrav.org/content/headers
title: Adding WAI-ARIA Landmarks to Joomla
slug: adding-wai-aria-landmarks-to-joomla
# menu: Adding WAI-ARIA Landmarks to Joomla
date: 16-05-2012
published: true
publish_date: 16-05-2012
# unpublish_date: 16-05-2012
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
    tag: [Accessibility,Joomla,wai-aria,Accessibility,Joomla,wai-aria]
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

In the world of accessibility, ARIA landmarks help screen readers identify common areas of the website in a consistent way. Users with assistive technologies can now use these landmarks to navigate to sections of a page's content. These landmarks are a vast improvement to the commonly used, “skip to content”, and “skip to navigation” commonly deployed prior to WAI-ARIA but personally I believe still shouldn't be disregarded.

Having landmarks on all websites will help assistive technologies provide a consistent user experience for this audience.

[![WAI ARIA Categorisation of roles](http://www.w3.org/TR/wai-aria/rdf_model.svg)  
](http://www.w3.org/TR/wai-aria/rdf_model.svg "WAI ARIA Roles categorisation")[http://www.w3.org/TR/wai-aria/rdf\_model.svg](http://www.w3.org/TR/wai-aria/rdf_model.svg)

 Class diagram of the relationships described in the role data model.

Adding these landmarks to your Joomla website is quite easy with the use of HTML overrides. These HTML overrides introduced with Joomla 1.5.x allows a web developer to replace the output of the Joomla code from any component or module with their own custom output, thus allowing for the addition of WAI-ARIA landmarks to be added to your Joomla website without the need for modifying the core code.

## Understanding Joomla HTML Overrides

To be able to add WAI-ARIA landmarks to a Joomla website you must first understand the concept of HTML Overrides and how to implement them to a Joomla template.

To find out more, please read [Joomla HTML Overrides and implementation explained](index.php?option=com_k2&view=item&id=340&Itemid=117 "Joomla HTML overrides explained").

## Modifying the Joomla Templates

With other areas of a Joomla website where we must modify the template output, we'll need to access the website's main template and add in containing divs or modify existing ones to add in WAI-ARIA landmarks.

## Different WAI-ARIA Landmarks

There are several common WAI ARIA landmarks that can be added to a Joomla website including:

- application
- banner
- complementary
- contentinfo
- form
- main
- navigation
- search

### Application

The application landmark represents an area of the website's page that is a software/application presented for a set of tasks for its users.

### Banner

Area that contain the main heading or internal page title. Usually contains the logo, site sponsor banners, main page title and search tools. Could also possible house a navigational menu.

### Complementary

Complementarty is a supporting area of the website such as side bar that contains meaningful information to the main area of the page. It could possibly contain, secondary navigation, related information or content.

### Contentinfo

Metadata that applies to the parent document. For example, footnotes, copyrights, and links to privacy statements would belong here.

### Form

Defines an area of the page where there is a form elements for user interaction and input.

### Main

This is the main content area of the page and there should be no more than one main defined on any page.

### Navigation

This can be the main website's navigation or the page document's navigation.

### Search

This landmark defines the website's search functionality area.

In this example of adding in WAI-ARIA landmarks to Joomla, we'll be adding in the most common landmarks found in most Joomla websites including banner, main, navigation, search and complementary.

## 

## Adding the a WAI-ARIA Landmark

Each module in the module positions of a Joomla website can be modified and have new HTML overrides added to them.

Lets have a look at the default installation of Joomla 2.5.0 as an example of areas where we can specify these roles.

[![joomla adding wai aria landmarks](wp-content/uploads/2012/05/joomla-adding-wai-aria-landmarks-580px.jpg)](wp-content/uploads/2012/05/joomla-adding-wai-aria-landmarks.jpg "Larger version of WAI-ARIA roles defined in Joomla")

Demo site available at: <http://demo17.cloudaccess.net/>

Lets start with the easiest landmarks to add with the Modules.

### Adding WAI-ARIA landmark to Joomla Search Module

Once you have found and copied the main template file of the Joomla search module as defined in the [HTML overrides tutorial](index.php?option=com_k2&view=item&id=340&Itemid=117 "HTML overrides in Joomla") for Joomla, you will find this code as the output at line 13.

**<div class=”search”>**

This is the opening div container to the search module.

Add in the role landmark role=”search” to the div like so:

**<div class=”search” role=”search”>**

and add the file back into your HTML overrides folder of your Joomla template.

You're Joomla website should now have the search role landmark added to the template.

Download the modified [WAI-ARIA search default.php HTML override file](wp-content/uploads/2012/05/mod_search.zip "mod_search WAI-ARIA landmark").

 

### Adding WAI-ARIA navigation landmark for Joomla

The menu module is usually the default module used in a Joomla website's navigation. On some website build it may be used multiple times on page layout to display menus and links to different areas of a website.

If we modify the default HTML override file and add in the navigation role then all of the menus on the website will be marked as navigation. In some situations you will only want one of the menu items marked as the website's navigation.

To give you more control over the override we will create a separate override template and assign only one module to have the new override with the WAI-ARIA navigational role. Yo can however use the template on multiple modules on a page is so required.

First start off by duplicating the HTML override of the module menu to your Joomla template. Please refer to the [HTML overrides creation tutorial](index.php?option=com_k2&view=item&id=340&Itemid=117) if you do not know how.

Once created, rename it from default to another name such as “waiaria”. This will let you identify the WAI-ARIA version of the html override.

at approximately line 15 of the file, you will find:

**<ul class=”menu”<?php**

This is the starting unordered list that creates a menu structure in Joomla. Before this line you will have to create a containing div with the navigation role. You will get something like this:

**<div role=”navigation”>**  
**<ul class=”menu”<?php**

You will now have to end the containin div or else your website's layout will break. At line 83 at the end of the file you will find:

**?></ul>******

add the closing div tag after this.

**?></ul>**  
**</div>**

Save the file and upload it back to your mod\_menu html override folder in your template.

Once this is done, your site won't automatically output the WAI-ARIA landmark until you set it.

In the administrator area of your website, navigate to Extensions->module manager and select your main website's navigation module.

On the right hand side of the modules parameters is the advanced settings. Expand these parameters and you will be presented with the option of changing the modules template from a drop down menu.

![joomla alternative html override template](wp-content/uploads/2012/05/joomla-alternative-html-override-template.jpg)

Choose the “waiaria” template that we have just created and hit save and close to apply it to the website.

You should now have applied the WAI-ARIA template and now have the navigation role added to your website's main nav area.

Download the modified [WAI-ARIA mod menu waiaria.php HTML override file](wp-content/uploads/2012/05/mod_menu.zip "mod_menu WAI-ARIA landmark").

### Adding WAI-ARIA Landmark to Joomla Login Form

As in the previous example where we create a separate WAI-ARIA template for a specific use, we'll repeat the steps in creating a custom HTML template override for the login form and call it “waiaria-login”.

In this file at line 13 you will find:

**<?php if ($type == ‘logout') : ?>**

add in the wrapping div tag with the form role.

**<div role=form”>**  
**<?php if ($type == ‘logout') : ?>**

and close the div after line 83 with the closing div tag.

**</form>**  
**</div> **

Save and upload the custom override to your template.

Navigate to your login form module under Extensions->Module Manager and click on your login form.

![joomla alternative wai-aria login template](wp-content/uploads/2012/05/joomla-alternative-waiaria-login.jpg)

Under advanced parameters choose the newly create WAI-ARIA login template and hit save.

Download the modified [WAI-ARIA mod login waiaria-login.php HTML override file](wp-content/uploads/2012/05/mod_login.zip "mod_login WAI-ARIA landmark").

### Final Modifications to the Main Template

The final role areas that we are going to add in this example are the banner role, complementary role and the main role. These landmark roles usually have to be applied to the template itself and will require a bit of knowledge in how Joomla templates work.

In the case of the default Joomla Beez template that comes with Joomla 2.5.x, the only file that you need to modify can be found in the beez tempalte folder, /templates/beez\_20/index.php

#### **Banner Landmark**

For the banner landmark we are simply going to add the role to the already existing Joomla header div. At line 113 you file find the main header div

**<div id=”header”>**

and add in the role

**<div id=”header” role=”banner”>**

and you're done with the banner landmark.

#### Complementary Landmark

At line 155 you will find the start of the left side bar of Joomla.

**<div class=”left1 ” id=”nav”>**

at the end of this add in the role

**<div class=”left1 ” id=”nav” role=”complementary”>**

 Once again, because this is an already existing div you do not have to add in an extra ending div.

#### Main Landmark

The final landmark that we are adding is the main landmark that defines the main content area of a page.

On line 166 of the index.php file you will find the opening main div container.

**<div id=”main” role=”main”>**

add in the role at the end,

**<div id=”main” role=”main”>**

There is no need to close the div as it is already an existing one that is closed.

Once you have added this last landmark role in your are done in modifying your website template for Joomla to have WAI-ARIA landmarks.

Download the [WAI-ARIA modified default Beez\_20 template](wp-content/uploads/2012/05/beez_20.zip "Joomla default Beez 2 template with WAI-ARIA landmarks").

Save and upload the file back to your server and test the site against your assistive technologies to make sure that the landmarks are working correctly.

## You're All Done!

All websites are different and you will need to make changes accordingly to your website. This example and tutorial whoever should give you an overview of the different methods required to add landmarks to various areas of your website.

If I have missed anything or haven't explained anything clearly, please don't hesitate to ask.

### Additional Useful Reading

- <http://www.paciellogroup.com/blog/2010/10/using-wai-aria-landmark-roles/>
- <http://www.html5accessibility.com/>
- [http://www.w3.org/TR/wai-aria/rdf\_model.svg](http://www.w3.org/TR/wai-aria/rdf_model.svg)
- <http://www.w3.org/TR/wai-aria/>