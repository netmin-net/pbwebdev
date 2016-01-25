---
# http://learn.getgrav.org/content/headers
title: VirtueMart SEO and removing DETAILS suffix from the SEFs
slug: virtuemart-seo-and-removing-details-from-the-sefs
# menu: VirtueMart SEO and removing DETAILS suffix from the SEFs
date: 14-05-2014
published: true
publish_date: 14-05-2014
# unpublish_date: 14-05-2014
# template: false
# theme: false
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration-status: review
    category: [E-commerce,Joomla]
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

Sometimes we have no choice but to work with an extension of component that we don't like using. It might not be a part of our workflow or systems and VirtueMart is one of them.

It use to be our shopping cart system of choice, with so many features and a lot of them out of the box, it was quick and easy to get VirtueMart up and working but there are issues when it comes to customising it and getting under the hood of the component.

Since VirtueMart 2, there have been some changes and improvements to how the search engine friendly URLs work in the component. In most situations it is fine and works quite well.

In this case we are trying to remove the extra suffix at the end of the product url, for example:

**http://sitename.com/product-category/product-name**-details.html

A neater URL would be to just have

**http://sitename.com/product-category/product-name**

and remove the trailing -details.html

We've found that it is possible to remove the **.html** as it is a part of the Joomla! Global configuration and turning off that switch would disable the appended **.html** but the remaining **-details** can't be removed from VirtueMart.

If you look into the SEO configuration of VirtueMart and turn remove **-details** from the suffix options, the website will not work. Product pages will not display and only category pages will display.

Taking a deeper look into the online forums and other people's issues around this we found on the [VirtueMart forums people having the same issues](http://forum.virtuemart.net/index.php?topic=111756.0), and having to deal with having the extra suffix at the end. No love with VirtueMart today alas.

If you're considering creating a shopping cart on Joomla!, we highly recommend either [MijoShop](http://miwisoft.com/joomla-extensions/mijoshop-joomla-shopping-cart "MijoShop") or [HikaShop](https://www.hikashop.com/). They're both much better solutions for Joomla! compared to VirtueMart.

HikaShop being a native Joomla! component and MijoShop being a component bridge between Joomla! and OpenCart.

 

### Reference articles

- [VirtueMart forums and support](http://forum.virtuemart.net/index.php?topic=111756.0)
- [InMotion Hosting – Virtuemart SEF URLS](http://www.inmotionhosting.com/support/website/joomla-25/virtuemart-search-engine-friendly-urls)
- [Comments on the VirtueMart forums about removeing -details](http://forum.virtuemart.net/index.php?topic=103199.0)

 