---
# http://learn.getgrav.org/content/headers
title: Mautic Integration with Shopify to Automate Marketing and Sales
slug: mautic-integration-with-shopify
# menu: Mautic Integration with Shopify
date: 04-03-2015
published: true
publish_date: 04-03-2015
# unpublish_date: 04-03-2015
# template: false
# theme: false
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration-status: review
    category: [Shopify]
    tag: [Shopify, E-commerce]
author: Peter Bui
metadata:
    author: Peter Bui
    description: Tracking users and shoppers on your Shopify website and creating automated marketing lead nurture campaigns around them.
    keywords: shopify, mautic, automated, marketing
    robots: index, follow
#      og:
#          title: The Rock
#          type: video.movie
#          url: http://www.imdb.com/title/tt0117500/
#          image: http://ia.media-imdb.com/images/rock.jpg
cache_enable: true
last_modified: true
---
Shopify is a fantastic software as a solution shopping cart system that we love using for our customers at PB Web Development. It takes away a lot of the maintenance required behind managing a shopping cart solution letting development teams concentrate on building new campaigns, features and additions to the platform and shopping cart website rather than pathcing, maintaining and providing support.

Mautic is another one of those tools that we love to use to help our customers build their customer base and convert them into loyal customers. It is by far the best open source automated marketing tool we have used in years.

## Integrating Mautic and Shopify to Create Sales Mastery

Shopify can easily talk to Mautic by embedding a little bit of code on your Shopify theme that will send over customer data as they register on the website.

Here is an example of what the code looks like and can be seen on the I Am Infusion website.

 
    <script>
     jQuery(function($) { $('body').append('<img src="http://mauticurl/p/mtracking.gif?firstname=' + encodeURIComponent('firstname') + '&lastname=' + encodeURIComponent('lastname') + '&email=' + encodeURIComponent('email@address') + '">'); });
    </script>

The code easily allows you to forward the data from the Shopify store over to Mautic with no extra effort required.

For support and help in regards to configuring the app in your Shopify store and your Mautic instance please create a ticket or submit a comment on this page.

This method is a slightly more technical method of integration and is still fairly limited in regards to what information is being passed through via the system.

What we have planned is to pass even more detailed.

## Whats Does It Mean to Integrate the Shopify and Mautic

Having both of the platforms talking to each other means that you now will have a really good understanding of your customers, how they use your website and potentially convert them into leads and sales.

Being able to create lead nurturing campaigns to help increase your conversion ratios on your e-commerce store goes hand in hand with any online marketing you may do.

## Contact Us

If you're interested in boosting your sales and increasing the conversion ratio on your Shopify website, <a href="/contact" title="Contact us">contact us</a>, and we'll help integrate Mautic and set up an automated marketing campaign to drive traffic and conversions to your website.