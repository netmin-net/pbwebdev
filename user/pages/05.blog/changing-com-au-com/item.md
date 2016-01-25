---
# http://learn.getgrav.org/content/headers
title: Changing from .com.au to Just a .com
slug: changing-com-au-com
# menu: Changing from .com.au to Just a .com
date: 20-08-2012
published: true
publish_date: 20-08-2012
# unpublish_date: 20-08-2012
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
    tag: [Domain Name,Domain Name]
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

![Domain name change overs](images/blog/2012/08/comau-com.png)

Some people may have noticed that we've been changing our main website URL from pbwebdev.com.au to just pbwebdev.com.

Why you may ask? Because we're starting to get a lot more international work and not just Australian based work and to better cater and target that audience we decided to refocus the domain branding to just .com.

## What's Involved?

There is actually quite a bit that needs to be done in order to transfer your domain name over from one domain to another.

Here is a check list of items that we recommend checking off when going through this process.

## Update Google Webmaster Tools

First step is to go about verifing your new domain in Google Webmaster Tools. Whether it is a change from a .com -> .com.au or .co.uk -> .com the process is all the same. Verify both the domains and make sure you also verify the www. versions as well as the non www. versions. This will give you more flexibility in terms of domain setups.

For PB Web Development we opted to have our domain setup without the leading www. This was to make marketing more consistent across Twitter, Facebook and print material where a few less characters makes quite a difference.

## Google Webmaster Tools Domain Change Over Request

Within Google Webmaster Tools you will have an option transfer domains. Once the new domain has been verified, the options will be available to point all the traffic from the old domain to the new. This process will take a few days to a few weeks.

## Resubmit Your Sitemap.xml File

Make sure that a new xml sitemap is generated and resubmitted to Google Webmaster Tools. This will ensure that all the URLs on your new website are being crawlled.

## .htaccess Update

Next is to setup the .htaccess file on your old website to point to your new.

You don't want to simply point all traffic to the new domain but point the old URLs to the same corresponding new URLs on the new domain name.

e.g. http://www.pbwebdev.com.au/blog redirect to pbwebdev.com/blog

Below is the htaccess script that we've used for our transfer. You'll need to adapt this for your own domain obviously.

Options +FollowSymLinks  
 RewriteEngine on  
 RewriteCond %{HTTP\_HOST} !^pbwebdev\\.com  
 RewriteRule (.\*) http://pbwebdev.com/$1 [R=301,L]

## Left Over PHP Redirects

Last but not least you'll need to add in a PHP 301 redirect to your Joomla template just incase your .htaccess file doesn't redirect all of your traffic.

Locate your index.php in your main template and add the header redirect code into the template.

header( “HTTP/1.1 301 Moved Permanently” );  
 header( “Location: http://pbwebdev.com” );

The htaccess file will redirect the all traffic to the new domain but if for what ever reason it doesn't work, this PHP 301 redirect will take care of any other Joomla page.

## Track Your Traffic

Over the next few weeks after launching the site on the new domain, make sure that checks are made on the server statistics to see where traffic is coming from and if any pages or content is still being called from the server. If there is, then do what is appropriate to point the direct the traffic to the new location.