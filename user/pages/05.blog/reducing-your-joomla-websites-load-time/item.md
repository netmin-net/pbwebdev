---
# http://learn.getgrav.org/content/headers
title: Reducing Your Joomla Website&#8217;s Load Time
slug: reducing-your-joomla-websites-load-time
# menu: Reducing Your Joomla Website&#8217;s Load Time
date: 13-09-2009
published: true
publish_date: 13-09-2009
# unpublish_date: 13-09-2009
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

So you've made your website, and it looks great! You've started to drive customers and traffic to your website but you're finding that the money that you're spending on pay per click advertising, search engine optimisation and online marketing isn't converting to leads or sales.

On close inspection of your web stats you may notice that there is a high bounce rate on your site or that people are only spending a few seconds on the landing pages of your site simply to exit on the same page. Other reasons could be usability and content on your site but we'll assume they're pretty spot on for the sakes of this article.

One cause for these high bounce rates is your websites load time. Almost everyone these days is lucky enough to have access to blazing fast internet connections where we can get anything on the web almost instantly, all at the same time. This is what web users are use to now and we need to make sure it is what we, as designers, developers and web managers, must deliver in order to satisfy these expectations.

So whats the big deal with speeding up the load time of a website?

What this article will cover.

- Basic Principles of Web Content Delivery
- Getting Joomla Ready for optimisation
- Optimising Templates and Site Content
- Server Optimisation
- .htaccess optimisation
- Tools

### Basic Principles of Web Content Delivery

**Server proximity**

Look at the target audience for your website. If you're target audience is in the UK, they you're better off getting a server in the UK than you would be here in Australia. It will be slower for yourself to use and manage the website but it will be much faster for your customers and web site users. Content Delivery Networks can counter act this and help speed up delivery of content around the world.

**Browser Connections**

Most modern web browsers will have 2 concurrent connections to a server. Firefox 3 has been upgraded to 15 concurrent connections and Internet Explorer 8 now has 6 concurrent connections.

This means that for any domain that it connects to, it will download 2 files from that server at a time. Splitting your content in to sub domains will increase the amount of connections for your website and thus increase the load time of your website.

**Combining Files**

Joomla sites rely on various CSS files to control the look and feel of the site and its modules and components.

You may find that there are several of these files on your site, each one of these files will add to your websites load time. Combining these files all in to one or two main CSS files win reduce the amount of connections required to render your site. This also goes for Javascript. You may have some issues in combining these files.

**CSS Sprites**

Creating a CSS sprite image will reduce the amount of connections needed.

[![Apple.com's Global Navigation CSS Sprite](wp-content/uploads/2009/09/globalnavbg-300x46.png "Apple.com's Global Navigation CSS Sprite")](wp-content/uploads/2009/09/globalnavbg.png)Apple.com's Global Navigation CSS Sprite



Many common practises saw each and every roll over state being an image. Each one of these images would be considered as an additional connection to the server and add to the load time. If you can combine several images in to one image, you can effective cut the amount of connections required down to just 1.

In the case of Apple.com's menu image sprite, in a worse case old style of CSS coding, it would have used 32 different images, an image for each roll over and active state. The image sprite reduces those connections from 32 to just 1.

**Compressing HTML, CSS and Javascript files**

There are several methods of compressing files for delivery. One main method that we use for compression CSS files is to combine them all in to one file, strip out comments and white space and then compress them for delivery with Gzip. For the sakes of this tutorial, we'll just briefly mention the method ad refer you to another site that has a complete tutorial on how to combine and compress files for delivery.

This is one CSS compression tool that we like to use to clean up CSS files and reduce their overall file size.

- [http://www.cssdrive.com/index.php/main/csscompressor/](http://www.cssdrive.com/index.php/main/csscompressor/ "CSS compressor tool")

Websitetips.com here will provide you with the complete compression, CSS combination and stripping.

- [http://websitetips.com/articles/optimization/css/crunch/](http://websitetips.com/articles/optimization/css/crunch/ "CSS crunching with php")

and another really good one from Ethan and Jamie

- <http://www.ethanandjamie.com/blog/43-web-dev-freebies/85-php-gzip-css-files>

and lastly

- <http://www.catswhocode.com/blog/3-ways-to-compress-css-files-using-php>

### Getting Joomla Ready for Optimisation

Now before we start anything, go out and download Firefox and these addons if you haven't done so already. They're all tools that will allow you to analyse your changes to your website and see exactly how much faster your site is as a result of your optimisation.

- FireFox
- Web Developers Toolbar
- Firebug
- YSlow plugin for Firebug

Now that you've installed all of those programs and addons go ahead with the initial check list.

**Initial check list**

- Enable Joomla's site cache and choose an appropriate cache time for your site. If you're site doesn't change often then it is probably safe to leave a fairly high cache expiry time. [![Enabling Joomla Site Cache](wp-content/uploads/2009/09/Picture-1-300x126.png "Enabling Joomla Site Cache")](wp-content/uploads/2009/09/Picture-1.png)Click to Enlarge – Enabling Joomla Site Cache
- Check all of your extensions and enable GZip options where possible. Disable javascript in the extensions and combine them in to your templates where possible. [![Click to enlarge](wp-content/uploads/2009/09/Picture-2-300x87.png "Module Cache")](wp-content/uploads/2009/09/Picture-2.png)Click to enlarge – Module Cache
- Enable module caching on your website's modules. Might break some layouts so do some testing.
- Optimising templates and content
- Combine your CSS and JS files where possible.
- Addon extensions, modules and plugins will sometimes use additional CSS and JS. Disable and remove if you're not using them.

### Optimising Templates and Site Content

**Template Check List**

- Combine CSS files
- Compress CSS files using Gzip
- Create CSS sprites, using CSS positioning.
- Repeating background images.

**Content Check List  
**

Creating subdomains for your content delivery is a common technique we like to use on some of our sites. It effectively create more connections available for your browser to download more images from your server.

Creating sub domain will work on your Joomla site like so.

http://www.site.com.au/images/stories/Joomla.jpg

call as

http://images.site.com.au/stories/Joomla.jpg

Be even more creative and call all your template files from a subdomain as well

http://templates.Site.com.au/TemplateName/css/templates.css

Optimise all of your images using tools such as Photoshop. Make sure you use PNGs, GIF and JPEG where appropriate.

Putting template and images off on a different server won't work as it creates another DNS lookup the the browser has to search for which will increase your load time rather then decreasing it.

### Server Optimisation

Move from a shared environment to a Virtual Private Server (VPS) or a dedicated environment to free up resources

Move your MySQL database to its own server. Can reduce server loads. Recommended for high traffic websites. This isn't the easiest process with Joomla but it can be done. We'll touch on this in another tutorial.

### .htaccess Optimisation

There are quite a few .htaccess tricks that can be used to help the reduction of server load and hopefully increase speed. One common .htaccess technique is to stop hot linking of images. The script below can be added to your .htaccess file to stop people linking to your content images from other server and hopefully reduce server usage.

    #disable hotlinking of images with forbidden or custom image option<br></br>
    RewriteEngine on<br></br>
    RewriteCond %{HTTP_REFERER} !^$<br></br>
    RewriteCond %{HTTP_REFERER} !^http://(www\.)?yourdomain.com/.*$ [NC]<br></br>
    #RewriteRule \.(gif|jpg)$ - [F]<br></br>
    RewriteRule \.(gif|jpg)$ http://www.yourdomain.com/stophotlinking.jpg [R,L]

### Resources and Links

- <http://www.catswhocode.com/blog/3-ways-to-compress-css-files-using-php>
- [http://www.cssdrive.com/index.php/main/csscompressor/](http://www.cssdrive.com/index.php/main/csscompressor/ "CSS compressor tool")
- [http://websitetips.com/articles/optimization/css/crunch/](http://websitetips.com/articles/optimization/css/crunch/ "CSS crunching with php")

### Tools

A brilliant tool that does most of the compression and combining of all the CSS and JS files for you.  
 \*NOTE: It may break your site and doesn't work in all cases.

[http://www.rockettheme.com/extensions-updates/495-rokgzipper-15-released](http://www.rockettheme.com/extensions-updates/495-rokgzipper-15-released "RocketTheme GZipper")