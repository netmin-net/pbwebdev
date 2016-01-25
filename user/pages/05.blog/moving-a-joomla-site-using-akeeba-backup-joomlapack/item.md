---
# http://learn.getgrav.org/content/headers
title: Moving a Joomla Site Using JoomlaPack
slug: moving-a-joomla-site-using-akeeba-backup-joomlapack
# menu: Moving a Joomla Site Using JoomlaPack
date: 09-04-2010
published: true
publish_date: 09-04-2010
# unpublish_date: 09-04-2010
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

In one of my previous posts on [migrating a Joomla website](http://www.pbwebdev.com.au/blog/migrating-joomla-websites-to-a-new-server.html), we looked at a manual method of migrating a web site using simple tools such as FTP programs and simple database access such as phpMyAdmin.

That was so 2008 and there has been much development since in terms of quickly and easily migrating your Joomla website from one server to another.

This tutorial will look at a new method of Joomla website migration using the JoomlaPack Backup extension, also known as Akeeba Backup. We'll also be rewriting our manual backup and migration process in another article.

## Assumed Knowledge and Technology

- Familiar with installing and configuring Joomla Components and extensions
- Using a Linux based server environment (LAMP) and also running a cPanel control area to administer your website.

Lets begin!

## Why Move Servers

There may be many reasons why your moving your Joomla site from one server to another.

- Upgrading to a new server with new resources
- Moving a Joomla site from a localhost development environment to a live environment
- Duplicating a Joomla site for a mirrored development, staging and live servers

## What You Need

First off is the JoomlaPack component files. These can be obtained from the Akeeba Backup web site at: <http://www.akeebabackup.com/download/joomlapack-241/index.html>

At the time of writing this tutorial, the latest stable version is JoomlaPack 2.4.1. Akeeba Backup is also avaliable but is still in its alpha stage of development so we won't quite use that version just yet for a production ready Joomla site.

- [Download](http://www.akeebabackup.com/download/joomlapack-241/index.html) and install the JoomlaPack component. Install the component as you would as Joomla component using the Extensions > Install/Uninstall part of the Joomla administrator area.

## Configuration

In most cases, JoomlaPack will work straight out of the box without any additional configuration, but there are a few steps that we like to do in terms of long term maintenance.

Navigate to the configuration screen of JoomlaPack. This can be found in the administrator area under:

Components > JoomlaPack > Configuration

[![Screen shot 2010-04-10 at 9.12.21 AM](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.12.21-AM.png "Screen shot 2010-04-10 at 9.12.21 AM")](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.12.21-AM.png)

First thing to change is the Output Directory of the backup files. We like to keep all of the backup files in the TMP directory of the Joomla site. e.g. /sitedomain.com/tmp. This helps us identify files that can be quickly removed from the server if need be.

[![Screen shot 2010-04-10 at 9.31.00 AM](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.31.00-AM.png "Screen shot 2010-04-10 at 9.31.00 AM")](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.31.00-AM.png)

- Browse to the TMP folder of your Joomla installation and click USE to configure JoomlaPack to use your Joomla site's main TMP folder for storing backups.

Next step is to check to make sure that the Archiver engine is set to ZIP.

[![Screen shot 2010-04-10 at 9.37.43 AM](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.37.43-AM.png "Screen shot 2010-04-10 at 9.37.43 AM")](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.37.43-AM.png)

- Profile Settings > ZIP (Using PHP functions)

We prefer to use the ZIP method as it gives us more options for handling the backup file later on.

## Backup Time

Now you're ready to start the backup process of the site.

Hit the Green icon that says, “Back Up Now” to start the process. You will be taken to another screen where you can add notes to your backup. There will be a warning stating that ZIP format is being used as the default backup format. Ignore this and hit backup now.

[![Screen shot 2010-04-10 at 9.39.10 AM](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.39.10-AM.png "Screen shot 2010-04-10 at 9.39.10 AM")](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.39.10-AM.png)

The component will slowly work its way through the site and backup your database and data files and compress them all in to the backup zip.

\*Make sure you do not navigate away from the page at this point in time until the backup is done.

You should see the screen update with the files and directories that are currently being backed up by JoomlaPack.

Once the backup is done, click on Administer Backup and download your newly created backup.

## Restoring the Backup on the New Server

This is where things may get a little bit more interesting.

The next part of the tutorial will assume that your new server is using a cPanel environment and that you know how to use some of the features in the cPanel.

- Login to the cPanel admin area of your new web server that you are migrating your Joomla site to.

Look for the file manager within the cPanel area of your site and load it up.

[![Screen shot 2010-04-10 at 9.40.46 AM](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.40.46-AM.png "Screen shot 2010-04-10 at 9.40.46 AM")](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.40.46-AM.png)

Navigate to the **root **public area of your site. This is usually **/public\_html**. Once you've reached this part of the site.

[![Screen shot 2010-04-10 at 9.41.45 AM](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.41.45-AM.png "Screen shot 2010-04-10 at 9.41.45 AM")](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.41.45-AM.png)

Click on the **upload **button at the top of the screen and you will be taken to the upload file part of your site. Click **browse **and navigate to the backup file that you have downloaded from JoomlaPack a moment ago and start uploading it to your new server. This may take awhile depending on how large your backup file is.

Once uploaded, close your upload file screen and return to the file manager screen. Refresh the view and you should see the zip file that you have just uploaded to the server.

[![Screen shot 2010-04-10 at 9.42.41 AM](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.42.41-AM.png "Screen shot 2010-04-10 at 9.42.41 AM")](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.42.41-AM.png)

Select the backup file and now click on the extract icon at the top of the screen.

Choose /public\_html/ as your output directory and wait a moment as the entire site is extracted to your new server.

\*Note: This is one reason why we choose to use ZIP as the archiving engine. You can simply use the Unzip function in the file manager. You can also SSH in to your server and run a unzip command line to extract all of your files to your server. Keeping it as a JPA file won't allow you to do this in most cases.

Now that all the files are on your server, you now need to set up the new database and database user in order finish the process.

[![Screen shot 2010-04-10 at 9.40.52 AM](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.40.52-AM.png "Screen shot 2010-04-10 at 9.40.52 AM")](wp-content/uploads/2010/04/Screen-shot-2010-04-10-at-9.40.52-AM.png)

Go back to your cPanel admin area of your server and locate MySQL Databases. Click the icon.

Here there are three things you will need to do in this order:

1. Create a new database. Write down the name of it to be used later.
2. Create a new user. Also write down the name of the user that you have just created as well as the password. (I hate it when I forget this as you will have to delete the user and recreate it again)
3. Link the user to the database.

Once this is done you will be able to start the JoomlaPack site restore procedure.

## JoomlaPack Restore Procedure

This restore procedure is very much like the initial installation of a clean Joomla site on to a server. This is probabbly why it is so popular as previously we would have had to manually restore the database, and then create the Joomla configuration file to match the settings of the new server. JoomlaPack Restore Procedure takes away these manual steps and presents them in a nice user interface.

So now, simple load your site in the browser by navigating to the domain name. e.g mywebsite.com. You should now be presented with the JoomlaPack installation procedure.

Simply follow the 4 steps entering all the required information. Remember how I mentioned to write down all of those database names, user details and passwords? This is why you needed to.

Finish the 4 step process and then remove the installation directory from your web server and you should have finished restoring your website on to your new server.

Perfecto!

You you have any questions about this method of Joomla site migration, please leave us a message and we'll get right back to you.