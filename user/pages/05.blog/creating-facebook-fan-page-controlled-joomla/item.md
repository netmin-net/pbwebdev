---
# http://learn.getgrav.org/content/headers
title: Creating a Facebook Fan Page Controlled by Joomla
slug: creating-facebook-fan-page-controlled-joomla
# menu: Creating a Facebook Fan Page Controlled by Joomla
date: 14-08-2011
published: true
publish_date: 14-08-2011
# unpublish_date: 14-08-2011
# template: false
# theme: false
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration-status: review
    category: [Joomla,Social Media]
    tag: [Facebook,Social Media,Facebook,Social Media]
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

Last month we received a bit of a response back from our template that we released for creating a custom Facebook landing page for fan page controlled by Joomla. The template itself is fairly simple and is basically optimised to look and feel right on a 520 px wide canvas that Facebook allow you to work with. You can download and find out more about the template from our [previous post on the fUser Template](blog/fuser-template-facebook-fan-pages "fUser Template for Facebook Fan Pages"). The biggest bit of feedback was, ahem, then lack of setup tutorial. So that is what this is. The rest of this post will take you through a step by step guide to help you setup and customised the fUser template for your website.

For the novice this might be quite a daunting process but if you follow the steps it should be fairly straight forward. It will help if you already have knowledge about managing templates, modules and content within your Joomla website.

- [Installing the template](#install)
- [Creating Modules and Content](#create)
- [Creating a URL for the Fan Page](#URL)
- [Setting Up the Facebook App](#facebookapp)
- [Linking It All Up](#linking)
- [Testing and Troubleshooting](#trouble)

<a name="install"></a>

## Installing the Template

Start by doing to the fUser template overview page and download the template to your computer. At the time of writing this tutorial there is only a version available for Joomla 1.5 but the process is pretty much the same for all versions of Joomla. Login to the backend of your Joomla website. **Navigate to Extensions->Install** Click on the browse button and browse to the location where you have saved the fUser template to your computer. [![Installing the fuser template for Joomla](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-4.50.14-PM.png "Installing the fuser template for Joomla")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-4.50.14-PM.png) Click **Install**and the Joomla will upload and install the template to your website.

[![fuser template installed](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-4.51.04-PM.png "fuser template installed")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-4.51.04-PM.png)

<a name="create"></a>

## Creating Content and Modules for your Fan Page

Now that the template is installed we'll need to start creating some content for the fan page. Create a content page for your Fan page whether is a Sobi page, k2 content item or regular Joomla content page. For the sakes of this tutorial well just create a temporary page that we can add more content to later.

[![Creating a content page in Joomla](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-4.57.09-PM.png "Creating a content page in Joomla")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-4.57.09-PM.png)

Some module position that you also might want to note that are avaibale in the template as well are fuser1, fuser2, fuser3 and fuser4. Each on of these module position represents a block above or below the main content area in the template. More can be added quite simply by anyone with the knowledge of how to edit Joomla templates. So next lets create a new latest news module for one of the module positions. **Click Extensions->Module Manager** on the far top right, click new and select from the list, **Latest News**. This particular module will allow you to create a list of links to the latest articles that you have create in a Joomla category. Fill in the category parameters for the module on the right.

[![Creating the lastest news module](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-4.59.01-PM.png "Creating the lastest news module")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-4.59.01-PM.png)

Then on the left under module “Details”, choose the position that you want the module to appear in. You may have to type in the position manually as it may not appear under the available positions just yet. In this case we are going to place the latest news content module under the main content block, so we're going to choose position. fUser3. I had to type it in for this example. Make sure the module position is enabled and hit save. Now you have some content placed together for your fan page. Next we'll need to create an accessible URL for the Fanpage and enable the fUser template to the URL. <a name="URL"></a>

## Creating a URL for the Fan Page and Assigning the fUser Template

Joomla required you to have a menu item for a particular page in order to assign a unique template to it. This is fine and actually perfect for our situation as well must assign the modules and template to this menu item as well. In the backend of Joomla, navigate to menu manager and create a new menu. Fill in the steps as follows to create the new menu block. We don't actually want this menu module or links to appear on the site so one common practice to to call this Hidden or Invisible to to remind and promopt you what this menu block is for. [![Creating a new menu](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-5.02.06-PM.png "Creating a new menu")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-5.02.06-PM.png)Create a new menu item as an direct link to a Joomla content article in this case. Give the menu item link a name of Facebook to easily make it distinguishable.

[![Adding the Facebook menu link](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-5.04.57-PM.png "Adding the Facebook menu link")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-5.04.57-PM.png)

Hit save and now to test on the website. If you have search engine friendly URLs turned on for your website then Joomla will most likely create your new page as http://www.yourwebsite.com/<menu item name>, where yourwebsite.com is the domain of your website and <menu item name> is the name of the menu item you just create in the above step, e.g. facebook. If this doesn't work then we have to go back and figure out what the Joomla URL is for the particular page. You can do this by going back into the Menu item that you have created and looking at the link URL that Joomla will provide you. Alternatively, you can create the link to this content item in your main website's navigation and then move it into the hidden menu list after you have grabbed the URL. This might be the easiest way for a novice Joomla administrator. Now that you have the Joomla page and menu item setup, it is time to assign the fUser template to the menu item. **Navigate to Extensions->Templates** in the backend of your Joomla website and select the fUser template. From here you will see some menu parameters on the bottom left of the screen. Choose, select menu item from the selection boxes and then navigate through the selection until you can see the newly created menu item for Facebook in the list.

[![Assigning the template](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-5.09.16-PM.png "Assigning the template")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-5.09.16-PM.png)

Select the menu item and hit save. This will assign the template to appear for this particular menu item. Repeat the process but this time for your modules. The module positions are unique to this template, hopefully, so you might not need to do this step, but if you are create more custom module positions or if you are using the Joomla loadposition plugin to load modules in your content pane then this step is necessary. **Navigate to Extentions->Module manager** in the backend of Joomla and navigate to the modules that you have create for the Facebook landing page. Repeat the same process of selecting the menu item to assign the module to and hit save. [![Assigning the modules](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-5.11.19-PM.png "Assigning the modules")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-5.11.19-PM.png)

Repeat this process for any modules that you want to appear on the fan page. Now that all of the Joomla side of things is setup we can move on to the slightly more tricky side of setting up the Fan Page. This is what our Fan page looks like at the moment. http://www.austconserv.com/facebook [![Current Fan Page](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-5.14.01-PM.png "Current Fan Page")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-5.14.01-PM.png)

Still quite a bit of customisation needed in the template's images and CSS still to remove the default branding.   <a name="facebookapp"></a>

## Setting Up the Facebook App

These next steps will take you through how to setup the landing page of your Fan page as a Facebook App. It might be worth noting that you may require the minimum of 25 likes to fully customise your Facebook Fan page. Visit the Facebook Apps developers page and start the process of creating a new app. [https://developers.facebook.com/apps](https://developers.facebook.com/apps "Facebook Apps Developer's page")In the top right of the screen click “Create New App” and give you Fan page app a name, e.g. “My Landing Page” for example.

[![Create a Facebook App](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-2.11.52-PM.png "Create a Facebook App")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-2.11.52-PM.png)

Once you've clicked continue, the App information screens will appear, fill in the About pages with appropriate information about your landing page app. At this point in time it isn't important and you can come back and do this later. From the side menu, select, “On Facebook”. From here you will need to fill in the details of the page tab URL. In this example it will be http://www.austconserv.com/facebook for the site URL and austconserv.com for the site domain. Give the Tab a name, and define the URL. The Tab URL relates directly to the URL that you created earlier on your Joomla website for the Facebook fan page.

[![Defining the Facebook Tab URL](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-2.25.43-PM.png "Defining the Facebook Tab URL")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-2.25.43-PM.png)

Hit the “Save Changes” button and this step is done.

\*Note: the secure URL will only work properly if you have a SSL certificate installed on your website's hosting environment.

<a name="linking"></a>

## Linking It All Up

Now on the left hand menu under “related links” click on the menu item, “View App Profile Page”, This will take you to the public overview page of the app. On the bottom left area of this page click on “Add to My Page”

This bring up a dialogue box with all the pages that you administer. Scroll down to the Page that you want this app to be on and click

[![Adding an App to a Facebook fan page](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-2.21.09-PM.png "Adding an App to a Facebook fan page")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-2.21.09-PM.png)

Hurray, just a few more steps and where there.

Now that the App is attached to your Fan page, navigate to your fan page and click on Edit in the top right. From the left hand menu on the edit screen choose Apps.

[![Adding Apps tab to Fan Page](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-2.29.18-PM.png "Adding Apps tab to Fan Page")](wp-content/uploads/2011/08/Screen-shot-2011-08-14-at-2.29.18-PM.png)

This will now add the Landing page to the side tab of your fan page. Users can now click on the link to the landing page which should be visible just under the main profile picture of your Fan page. Now, last and not least, you need to make the Joomla powered fan page the default tab that new visitors will see when coming to your Fan page. Click on “Manage Permissions” from the edit page left hand menu. There you will see the option to choose the “Default landing tab”. Choose the newly added tab, in this example, AustConserv and you're done. You've now added the Joomla powered page to to your Fan page in Facebook and have made it the default landing page for new users. Ending result: [http://www.facebook.com/austconserv?sk=app\_179698512098370](http://www.facebook.com/austconserv?sk=app_179698512098370) <a name="trouble"></a>

## Testing and Troubleshooting

Some issues that you might come across include assets being pulled from non secure servers when a Facebook user is logged in under the secure server, https://. This is a little bit unavoidable with this setup. You're users will still be connected to Facebook securely but the content on the Fan page won't be coming from the same server and if you don't have a SSL certificate, the content won't be pulled in securely either. Other issues that might occur is the opening of pages from your landing page. All pages should be set to “open in new window”. This will avoid the links opening up in the limited Facebook Canvas. We've provided a few HTML overrides in the template that will take care of this for some of the modules that you might use. If you really want a particular module overridden then we may also include it in the distribution if there is demand for it. Beside those know issues, please post what else you might stumble across. All feedback and reviews are most welcome.