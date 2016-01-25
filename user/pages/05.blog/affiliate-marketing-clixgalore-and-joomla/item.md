---
# http://learn.getgrav.org/content/headers
title: Affiliate Marketing ClixGalore and Joomla
slug: affiliate-marketing-clixgalore-and-joomla
# menu: Affiliate Marketing ClixGalore and Joomla
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
    category: [Uncategorized]
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

Affiliate marketing is a great way to increase the sales of your site and make extra money. This is both true for the advertisers and the affiliates that use the programs.

Being able to get extra sales with little effort is every shop owners dream. Why market your product when you can get someone else to do it for you. I know everyone has seen those penis enlargement emails and landing pages that have been float around cyber space.

Joomla has a fantastic shopping cart component called [VirtueMart](http://dev.virtuemart.net/cb/wiki/1381#section-What+is+VirtueMart_3F), it self has a built in affiliate program system but the third party affiliate programs on the net seem to do a pretty good job or marketing the programs to other webmasters.

The more webmasters that can see your affiliate program then the more money you can make in the long run. So, its best to take advantage of these third party players.

One that we'll be looking at in this article is [ClixGalore](http://www.clixgalore.com/).

### Overview of how they work

ClixGalore works by dropping cookies on to a users browser. The cookie stores the following information.

> Name: ClixGalorePercentSale9400  
>  Content: AffProgID=167218&AdvProgID=9400&BannerID=83063&  
>  IPSource=121.45.98.117&  
>  AffOrderID=&ClickDate=2008-4-11%208:37:34&  
>  RefSource=http://peter.pbwebdev.com.au/index.html  
>  Host: www.clixgalore.com  
>  Path: /  
>  Send for: Any type of connection  
>  Expires: Mon, 26 May 2008 5:15:03 PM

Let's have a closer look at the cookie information.

Name; well thats pretty obvious. It stores the name of the cookie and what type of cookie it is and who the affiliate sale is for. In this case its Merchant advertiser 9400, Bloom'a'lcious.

Content; this one is a little more tricky. This part of the cookie stores just about everything else from the Affiliate program ID, Banner Id, IP of the source cookie, click date of the banner click through and of course the source of the click through. All important statistical information that is also passed back to the main central ClixGalore database.

Expires; this is the last important part of the cookie. This tells the browser when to expire and get rid of the cookie. The life of the cookie is specified by the Merchant advertiser and define by their referral program conditions.

Now that the cookie is stored in to the user's browser, sales are now continuously tracked from here on in until the cookie expires. In this case it will expire on on, 26 May 2008 5:15:03 PM.

Oh, and of course, clicking on the banner also takes you to the merchant's site.

### The tracking code

Now, on the website of the merchant advertiser there needs to be a little bit of code that tracks the sales. For each sale that is made on the site that is done on a browser that has the stored cookie, it will pass the sale amount and the order or tracking id to the ClixGalore database. From here the sales are approved by the merchant advertiser. They would match and check that sales are actually being made from the referring site.

Now, ClixGalore does this tracking by having a small image file that passes these variables to the main server. The variables that are passed include the advertiser id, order amount and order id. These values seen to always be passed to the ClixGalore servers whether its an affiliate sale or not, but is only recorded it it is.

### Installing the tracking code on VirtueMart

Installing the tracking code is quite simple. You just have to know what variables need to be passed and how to get them but first of all, a little disclaimer.

### Disclaimer

*Now I have to warn you, playing with your VirtueMart files, especially if you don't know what you're doing will harm and may even destroy your site. Please please please don't mess with the files if you don't know what you're doing. I'm not responsible for the total destruction of your site.So please take care in editing your site files and make sure you back up. How about contacting a specialist to help you with installing the code. someone like, [me](http://pbwebdev.com.au/) :).*

OK, first of all open the file:

> /components/com\_virtuemart/html/checkout.thankyou.php

It would probally be best to make a backup at this point of the file.

As a merchant advertiser, you should have received a little bit of code that might look something like this:

> <!–begin clixGalore code copyright 2006 –>  
>  <img  
>  src=”/[https://www.clixGalore.com/AdvTransaction.aspx?AdID=XXXX&  
>  SV=SALE\_AM](https://www.clixgalore.com/AdvTransaction.aspx?AdID=XXXX&SV=SALE_AM)OUNT\_HERE&  
>  OID=AN\_ORDER\_ID” height=”0″ width=”0″ border=”0″>  
>  <!–end clixGalore code –>

So this is what you'll need to replace in those lines of code.

Firstly, add in your advertiser id or else your sale won't be marked to you, feel free to place in someone else's id but i suggest not. Replace XXXX with your advertiser id. For the sake of the example well make it 1234.

> <!–begin clixGalore code copyright 2006 –>  
>  <img  
>  src=”/[https://www.clixGalore.com/AdvTransaction.aspx?AdID=**1234**&](https://www.clixgalore.com/AdvTransaction.aspx?AdID=XXXX&SV=SALE_AM)  
> [ SV=SALE\_AM](https://www.clixgalore.com/AdvTransaction.aspx?AdID=XXXX&SV=SALE_AM)OUNT\_HERE&  
>  OID=AN\_ORDER\_ID” height=”0″ width=”0″ border=”0″>  
>  <!–end clixGalore code –>

Next is to place the order id and the order amount in to the code. Replace SALE\_AMOUNT\_HERE with $CURRENCY\_DISPLAY->getFullValue($db->f(“order\_subtotal”)) and replace AN\_ORDER\_ID with $db->f(“order\_id”).

> <!–begin clixGalore code copyright 2006 –>  
>  <img  
>  src=”/[https://www.clixGalore.com/AdvTransaction.aspx?AdID=**1234**&](https://www.clixgalore.com/AdvTransaction.aspx?AdID=XXXX&SV=SALE_AM)  
> [ SV=$CURRENCY\_DISPLAY->getFullValue($db->f(“order\_subtotal”))](https://www.clixgalore.com/AdvTransaction.aspx?AdID=XXXX&SV=SALE_AM)&  
>  OID=$db->f(“order\_id”)” height=”0″ width=”0″ border=”0″>  
>  <!–end clixGalore code –>

Now paste that bit of code near the ending display area or under the debugging code in the VirtueMart file and you should be good to go.

Do a few test transactions, even sign up as an affiliate to make sure that it is all working. Oh, and don't forget to delete your cookies while doing test transactions. Just to make sure that they are working right too.

### References

- [Installing ClixGalore affiliate tracking code](http://forum.virtuemart.net/index.php?topic=30187.msg120555)
- [ClixGaloreTutor – How to set up your tracking code](http://clixgaloretutor.com/how-to-set-up-your-tracking-code.shtml)