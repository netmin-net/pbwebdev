---
# http://learn.getgrav.org/content/headers
title: Next &#038; Previous Links Out of Order
slug: next-previous-links-out-of-order
# menu: Next &#038; Previous Links Out of Order
date: 19-11-2012
published: true
publish_date: 19-11-2012
# unpublish_date: 19-11-2012
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
    tag: [Joomla,K2,Joomla,K2]
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

![Previous next buttons in Joomla](wp-content/uploads/2012/11/buttons.jpg)Recently we've come across a little issue in Joomla that users were having where the articles in a category would be displaying in the wrong order or wrong sequence when clicking or navigating through them with the previous and next pagination links at the bottom of an article or an item.

This isn't quite an issue with Joomla itself but more so the understanding of how Joomla works and how menu links and content is organised in a Joomla powered website.

These instructions and explaination of content structuring and ordering apply for both the standard Joomla article manager as well as the K2 item manager in Joomla. We will be referring linking to pages as linking to articles/items to cater for both the standard core and the additional K2 content construction kit.

## Fixing Articles and Items that are in the wrong order with clicking on the Previous and Next buttons at the bottom of the page in Joomla

Lets start by looking at a standard menu structure and a standard article/item ordering that you might find in a category within Joomla.

**Menu structure**

- Menu link 1 -> Article/item 1
- Menu link 2 -> Article/item 3
- Menu link 3 -> Article/item 2
- Menu link 4 -> Article/item 4

What we are seeing here is a list of menu items that may be created in the menu manager of Joomla linking to individual articles or items in Joomla. The user has created the 4 menu links in the order that they want and has created the menu links to them accordingly.

When a front end user now navigates to “Menu link 1” then will be presented with “Article/item 1” but when they start to use the “next” navigational links at the bottom of the article/item the won't be taken to “Menu Link 2”, which should point to “Article/item 3” but instead be taken to Article/Item 2.

This isn't want the original site administrator intended as when you look at the menu structure the ordering of the Articles/items as you navigate through them sequentially should match.

This isn't an issue with Joomla itself but with the ordering of the Articles/items in the backend of Joomla.

The previous and next navigational links will simply display the next and previous items in the order that they appear in the backend of Joomla and not match the ordering that is set in the menu. In many situations you won't see individual links from the menu structure linking to each individual Article/item in Joomla but instead a menu item linking to a top partent item in Joomla which usually is a category view of all Articles and items in that category, e.g. Blog category showing all the blog posts within it. The previous and next links in this situation will sequentially navigate from one Article/item to the next according to when they were written or added into the category of the CMS.

This is the right and intended usage of the previous and next links.

We can however change the Article and item ordering in the previous example in order to have the correct previous and next navigation through our category and match that of the menu.

## Article/Item ordering in the Category

**Category Name**

- Article/item 4
- Article/item 3
- Article/item 2
- Article/item 1

What we are seeing here is the Article/items being added in date order as they are entered into the system with 1 being the first added and now being at the bottom of the category list. This is correct and how you would see most Joomla articles/items in the backend of Joomla.

Or course this will create ordering issues with the menu linking example above as the menus are linking to the articles in a different order.

To change this we must to two things. In Joomla for the articles you need to

1. Set the global ordering to category ordering
2. Reorder the articles in category to match that of your menu system

Within K2 you simple need to reorder the items in the category by first selecting the category that you are reordering and then select the order column to display the items by order.

To set to global shared ordering in Joomla, navigate to the Article Manager, click the options icon on the top right of the screen, then choose “Shared Options” and make sure that the option for “Category Order” is set to “Category Manager Order”.

![article-previous-next-pagination](wp-content/uploads/2012/11/article-previous-next-pagination.png)This will make sure that the Articles are being shown in the order that they are listing in the category. Next you will need to simple reorder the articles in the category in the order that you wish for them to appear. In the case of our example you will be swapping “Article/item 2” around with “Article/item 3” to make the previous and next links work in the right order.

If you have any questions or feedback please leave a comment or an email!