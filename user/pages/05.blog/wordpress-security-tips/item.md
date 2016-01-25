---
# http://learn.getgrav.org/content/headers
title: WordPress Security Tips
slug: wordpress-security-tips
# menu: WordPress Security Tips
date: 30-08-2010
published: true
publish_date: 30-08-2010
# unpublish_date: 30-08-2010
# template: false
# theme: false
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration-status: review
    category: [Security,WordPress]
    tag: [Website Security,WordPress,Website Security,WordPress]
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

There are a few easy steps that you can take to minimalise the chances of your unsolicited intrusions and failures to your website.

Follow these instructions to help improve your security and stop your WordPress site from being hacked.

## Upgrade WordPress

Making sure that your WordPress installation is up to date will make sure that any known security issues in WordPress are all patched up. Not upgrading to the latest stable versions will leave you open to these hacks and potential security threats.

### Upgrading WordPress Instructions

When a new version of WordPress is released, a message will display on the back-end of your website:

[![Update your WordPress installation](wp-content/uploads/2010/08/wordpress-security-01.png)](wp-content/uploads/2010/08/wordpress-security-01.png)WordPress Update Notification



Click “Please update now”, and then click “update automatically” when the next screen appears.

After a few moments, WordPress will let you know that the upgrade was successful, and prompt you to upgrade your database. Click yes, and after a few moments you will be ready to start using the latest version of wordpress on your web site. Easy!

In some situations you may have to do a manual upgrade of your WordPress website. In these situations you may need to call upon some web support to be able to do so.

## Upgrade Plugins

It's important to update your plugins to ensure that your website maintains the most current security measures, and minimalises the chance of any outside intrusions to your website.

By clicking on the “Plugins” button in the left hand column you can access the list of plugins that your site employs.

Certain plugins may require an update, and they will notify you of this by displaying a small window of text, as follows:

[![WordPress plugin update notification](wp-content/uploads/2010/08/wordpress-security-021.png)](wp-content/uploads/2010/08/wordpress-security-021.png)WordPress plugin update notification



Likewise, you might notice a number contained within a circle next to the “Plugins” button in the left hand menu. This is letting you know that you have some plugins that need to be updated. It‚Äôs a very simple procedure.

[![WordPress Plugin Notifications](wp-content/uploads/2010/08/wordpress-security-03.png)](wp-content/uploads/2010/08/wordpress-security-03.png)WordPress Plugin Notifications



By clicking “Upgrade Automatically” for each plugin, WordPress will install the required updates and give you a confirmation a few moments later.

## Change Your Password

It‚Äôs always a good idea to change your password to the backend of the website frequently.

Click “Users” from the menu on the left hand side., and click your name from the list of users that appears.

The screen that appears allows you to change some of your user information. You will need to scroll down the page to access the option to change your password.

When choosing a new password, it is good practice to use a combination of numbers, letter, symbols, small caps, and large caps. The more nonsensical your new password is, the more secure it may be. Choosing words that can be found in the dictionary is considered bad practice and unsecure.

## Backup

It‚Äôs important to back up the database of your wordpress site. This ensure that if anything catastrophic was to happen to your site you would still have a complete record of all your sites content that can be easily installed into the site site again.

We recommend automating the back up procedure, so you many never need to think about it. A great wordpress plugin to do this is “WordPress Database Backup”, and can be found at: <http://austinmatzko.com/wordpress-plugins/wp-db-backup/>

Once you have installed and activated this plugin via the plugins menu button (in the left hand menu), you can access the plugins settings by clicking **Tools **from the left hand menu, and selecting **Backup** from the small drop down list that appears.

Amongst the options that appear on the next screen, select “Email backup to:” and enter your email address, and select a time schedule (further down the page).

[![WordPress Backup](wp-content/uploads/2010/08/wordpress-security-04.png)](wp-content/uploads/2010/08/wordpress-security-04.png)WordPress backup settings



- TIP: It may be a good idea to send your backups to an email address that does not belong to your site. In the event that the entire website was hacked, it would be comforting to know that your backups had been sent automatically to an unrelated email address.

## Protecting the WP-CONFIG.PHP file

If you are a little more comfortable with accessing the server via FTP, then a handy trick is to secure the wordpress configuration file by writing a small .htaccess file and placing it in the root directory of wordpress.

Open up notepad (or your text editor of choice) and copy the following code:

 
     # to protect wp-config.php
    <Files wp-config.php>
    order allow,deny
    deny from all
    </Files>

Save the file to your desktop as htaccess.txt, and upload it to the root directory of your wordpress installation. Once uploaded, rename the file placed on the server to .htaccess

These are very simple steps that any website admin can do to help protect their WordPress website.