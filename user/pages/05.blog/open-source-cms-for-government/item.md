---
# http://learn.getgrav.org/content/headers
title: Open Source CMS for Government
slug: open-source-cms-for-government
# menu: Open Source CMS for Government
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
    category: [PB Web Dev]
    tag: [CMS,CMS]
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

[![Australian Government Logo](wp-content/uploads/2011/04/australia-government-logo.jpg "Australian Government Logo")](wp-content/uploads/2011/04/australia-government-logo.jpg)When it comes to designing and developing websites for Government, there are a few factors that have to be taken into account. Certain aspects such as web accessibility, accountability and internal workflow and processes all need to be looked at when building a site for a Government client/agency.

Here at PB Web Development we use two main open source platforms to deliver websites that meet certain Government requirements. Joomla is the main CMS that we use for our Government clients and Drupal for more complicated websites builds.

\*If you read this article before I proof read it, apologies.

## Features of Government Powered Joomla Website

### Security

First and upmost is security of the website. When delivering a Joomla website for Government, all security holes from the server to the instance of the content management system (CMS) all have to be looked at. Latest versions of the CMS, latest and secure extensions, locking down the CMS, file permissions and the server itself should be the first starting point for delivery.

For our Joomla powered websites, we have a list of security processes that we follow.

1. Proper secure server running the latest versions of a LAMP stack.
2. Lock down access to the website by IP address, making it only accessible from certain IP addresses. This is done on both a server and at CMS level.
3. Password strength and multiple passwords for access. This is sometimes painful for our clients but having multiple levels of passwords helps ensure that the blocking of illegal access.
4. Auto IP banning and auto flood protection. This helps identify illegal or suspicious activity from a certain sources and automatically blocks the access from that IP address.

### Publishing Workflow

Another feature that we have implemented in our Government Joomla builds is a workflow publishing system for content within Joomla. Being able to preview content on a staging environment to have it approved internally before it is made to go live is essential in a Government organization. In fact any high profile company that needs to have content checked before if goes live should have this processes in place.

![Update to Live](wp-content/uploads/2011/04/update.jpg "Update to Live")

### Tracking Access Logs

Tracking who accesses what within a system holds people responsible for their actions. We find it an important feature in our Joomla builds to know what user are accessing what content and where mistakes are made. This doesn't mean that you can blame someone for making mistakes that are being made on the website, but rather pin point where mistakes are being made and determine if further training in the CMS is required to reduce mistakes and incorrect actions in the future.

### WCAG Compliancy

Since all National Government agencies must comply with the WCAG 2.0 accessibility guidelines since it's announcement back in Feb 2010, all of the Joomla templates that we build at PB Web Development for our Government clients have to meet the guidelines.

For more information about the Australian Government strategy for transition to WCAG 2.0 please visit [Media Access](http://www.mediaaccess.org.au/latest_news/policy-legislation/australian-government-releases-adoption-and-implementation-strategy-for-wcag-20) for a run down on the National Transition Strategy.

Not all State Governments have applied the requirement to meet WCAG 2.0 yet but moves are being made to make sure that all websites are compliant in the future.

- <http://agimo.govspace.gov.au/2010/10/21/new-wcag-2-0-techniques-released-by-the-w3c/>

### Tiered Delivery of Sites

To make testing and easy on a Government CMS we've setup multiple instances of the one websites with different purposes for each one. This allows for website administrators to freely build and play around with the systems without the worry breaking a live production website.

### Content Delivery Networks

Did you know that the distance from Sydney to Perth adds at least 200 ms and more to the server response time? To get content delivered as fast as possible, we setup content delivery locations for the Government websites that we build. These are on Macquarie Telecom's infrastructure which offers a huge amount of bandwidth and great latency speeds across Australia. This will ensure that content is delivered from the closest cached location to the users computer as possible.

In Australia, there aren't too many companies that offer an Australia specific CDN but there are a few and the speeds that it delivers the Joomla site makes it worth using.

### Access Level Control

With the latest release of Joomla 1.6 also comes access level control. This gives website administrators full control over who can access what within the website. This is great for locking down areas of a websites to certain Departments within the Agency.

With some of our builds in Joomla 1.5, we have implemented some simplified access level control to restrict access to certain users.

 

## Some Australian Government Websites Powered by Joomla

So now you know what Joomla can do for your Government website. How about some examples?

- Independant Commission Against Corruption – <http://www.icac.nsw.gov.au>
- High Court of Australia – <http://www.hcourt.gov.au>

and more can be found at: [http://docs.joomla.org/Government\_Websites\_Using\_Joomla#Australia](http://docs.joomla.org/Government_Websites_Using_Joomla#Australia)

So if you're looking for an open source content management system as an alternative to corporate CMS solutions for a Government build, please consider using Joomla. You might be pleasantly surprised how well it can meet the the desired requirements.

Australian Government Webguide – <http://webguide.gov.au/>