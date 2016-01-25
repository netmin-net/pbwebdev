---
# http://learn.getgrav.org/content/headers
title: Migrating Joomla Websites to a New Server
slug: migrating-joomla-websites-to-a-new-server
# menu: Migrating Joomla Websites to a New Server
date: 24-06-2009
published: true
publish_date: 24-06-2009
# unpublish_date: 24-06-2009
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

> I've just rewritten this tutorial using JoomlaPack. So if you're familiar with using JoomlaPack and would like to learn how to use it to migrate to another server please read the new tutorial on [moving a Joomla site to a new server using JoomlaPack](http://www.pbwebdev.com.au/blog/moving-a-joomla-site-using-akeeba-backup-joomlapack.html).

Migrating a Joomla website from one server to another is a very easy process. It shouldn't take very long but there are various occasions where migration might cause a head ache or two.

There are six important steps that you'll have to follow for your Joomla server migration.

This tutorial assumes that you know a little about server management and the usage of FTP and phpMyAdmin, oh and that you are using Joomla 1.5.x. You will also need all of the details of your new and old server to be able to access all of the files and the database. So lets begin…

### 1) A backup of all your files

This can be done simply by logging in to your web site via FTP or via its control panel and downloading all of the files. I personally like to use a FTP program such as FileZilla, SmartFTP or FireFTP that integrates itself with FireFox. Make sure you get all of the files in your live public directory. Majority of servers either have a default public directory of “public\_html” or “html”.

If you are migrating from a local development server you should be able to get easy access to your files for migration.

### 2) Database backup

This step is a little tricky but it is made easier with a few tools and components that you can get to install on to your site. Basically what you'll need is a complete dump of your site's database. I like to use phpMyAdmin personally but you can get a dump of the database anyway you want. Some tools that you can install in to Joomla that will make the process easier include:

- [LazyBackup](http://extensions.joomla.org/component/option,com_mtree/task,viewlink/link_id,4445/Itemid,35/ "Lazy Backup") and
- [JoomlaPack](http://extensions.joomla.org/component/option,com_mtree/task,viewlink/link_id,1606/Itemid,35/ "JoomlaPAck")

With these two tools you can not only pack and download your database for migration but also set them up for automated backups.  
  
 LazyBackup is a fantastic and simple database backup tool for Joomla that posts the backups to your email address that you can define in the plugin's configuration. Backing up your site has never been so easy. The plugin also works natively in Joomla 1.5.x.

JoomlaPack is a more robust AJAX driven component that also allows you to backup all of the files on your site. This is also useful as it allows for the complete download of your site's files in one fast download.

### 3) Upload your site

Next you'll have to FTP in to your new server and upload all of your files. This is a pretty easy and straight forward step. Just the opposite of backing up and downloading all of your files from your old server.

### 4) Database migration

So this bit is a little tricky. The easiest way is to use a database tool such a phpMyAdmin. This will allow you to create a new database and then simply upload the backup that you have made to it.

Most modern web hosts will have phpMyAdmin installed as a default feature of your services. If you don't, ask for your host to install them.

If you're migrating to your own host and you don't have phpMyAdmin yet, simple [download](http://www.phpmyadmin.net/home_page/downloads.php "phpMyAdmin download") it from the site and install it to your server. It's another great open source project.

Alternatively you can telnet in to your server and run your MySQL commands to upload your database to the new server. This is alot more complicated and pretty time consuming if you don't know what you are doing.

### 5) Updating the configuration

Now the last thing you'll have to do is update the configuration.php file in your site and re upload it to your server. You'll need to update all of the database related information including the new database name on your server, username and password.  
  
 This is enough to get your site back up and running on your server. You'll will then have to change all of the log directories and the temp folders to match that of your new server as well. Once you've update just upload it all to your new server and you should be ready to go.

Here is a list of all the variables that you are most likely going to need to change and update to match your new server

> var $log\_path = ‘/;  
>  var $tmp\_path = ‘/';  
>  var $ftp\_enable = ‘1';  
>  var $ftp\_host = ‘;  
>  var $ftp\_port = '21';  
>  var $ftp\_user = ”;  
>  var $ftp\_pass = ‘;  
>  var $ftp\_root = ‘/';  
>  var $dbtype = ‘mysql';  
>  var $host = ‘localhost';  
>  var $user = ”;  
>  var $db = ”;  
>  var $dbprefix = ‘jos\_';  
>  var $password = ”;

Here is an explanation of each of the variables to help you on your way.

**$log\_path **  
 This is the default location where your log files are kept. A common log path would look something like this “/home/accountname/public\_html/log”

**$tmp\_path**  
 The tmp path is where temporary files are stored during the installation of components, backups, modules and plugins. “/home/accountname/public\_html/tmp”

**$ftp\_enable**  
 It might be best to have this switched off and set to 0 as a start. If this is set to 0 then the other variables, $ftp\_user, $ftp\_pass and $ftp\_root will not have to be set.

**$ftp\_port**  
 This is the default value for your FTP port. It is usually set at 21

**$ftp\_user**  
 This is the username for the accounts FTP

**$ftp\_pass**  
 The password for the ftp account

**$ftp\_root**  
 This is the root level of your site. In most cases it will be as follows “/home/accountname/public\_html/” Replace accountname with the appropriate account name and path.

**$user**  
 This refers to the username of the database that you would have set up in phpMyAdmin on your new server

**$db**  
 This refers to the database name of the new database that you would have set up on your new server

**$dbprefix**  
 As a default this is “jos\_”. to help increase security on your sites, you may wish to change this to something else to increase the level of security on your website.

**$password**  
 This is the password that relates to your database.

### 6) Updating Folder Permissions

If you are using Joomla 1.5.x and have FTP enabled on your site then you should not have to do this step as the system itself can simply overide permissions and do what it needs to do.

If you don't or you are having some issues with folder permissions then you'll need to update the permissions to some of the folder in your installation directory.

These include:

/cache  
 /tmp  
 /log  
 /images

You'll need to change the permissions on these folders to 755 or all read and write. This previously read 777 and as a security measure, it should be set to 755. Under no circumstance should any folders in your Joomla installation to 777.

If you're changing from one live server to another then you'll have to update the name servers for your domain and that is a little beyond the scope of this step by step tutorial but if you're migrating from a local development server then you should be all ready to go.

### Other uses: Custom base installations

So now that you know how to pack a site and move it to a new server you can also use this method to create default installations.

Migrating a Joomla 1.0.x installation is pretty much the same. Using FTP and phpMyAdmin is usually all you need.

At PB Web Development we have pre packaged installations of Joomla that have a selection of our favourite components, modules and plugins that allow us to create and modify our Joomla installations the way we want them. We found that the default installation has way too many unnessesary content and menu items that need deleteing.

Good luck and keep Joomlaing.