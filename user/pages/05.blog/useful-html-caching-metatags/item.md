---
# http://learn.getgrav.org/content/headers
title: Useful HTML Caching Metatags
slug: useful-html-caching-metatags
# menu: Useful HTML Caching Metatags
date: 21-08-2012
published: true
publish_date: 21-08-2012
# unpublish_date: 21-08-2012
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
    tag: [HTML,HTML]
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

We've been going a lot of work lately with site optimisation and debugging other sites that don't quite seem to work the way we want when caching is turned on too high.

There are a few HTML metatags that we've found useful to cache or not to cache your website's HTML pages.

Additional conditional statements in PHP can be used to turn these tags on and off in a Joomla website to allow better and more granular control of when these metatags may appear on the website. For example, if you don't want the component com\_contact being cached, you can write a simple conditional in the header of your Joomla template to detect when com\_contact is being displayed and echo the required metatags for caching.

## Cache-Control No-Cache

**<META HTTP-EQUIV=”CACHE-CONTROL” CONTENT=”NO-CACHE”>**

HTTP 1.1. Allowed values = PUBLIC | PRIVATE | NO-CACHE | NO-STORE.

- Public – may be cached in public shared caches
- Private – may only be cached in private cache
- no-Cache – may not be cached
- no-Store – may be cached but not archived

The directive CACHE-CONTROL:NO-CACHE indicates cached information should not be used and instead requests should be forwarded to the origin server. This directive has the same semantics as the PRAGMA:NO-CACHE.

Clients SHOULD include both PRAGMA:NO-CACHE and CACHE-CONTROL:NO-CACHE when a no-cache request is sent to a server not known to be HTTP/1.1 compliant.

Note: It may be better to specify cache commands in HTTP than in META statements, where they can influence more than the browser, but proxies and other intermediaries that may cache information.

 

## Expires

**<META HTTP-EQUIV=”EXPIRES” CONTENT=”Mon, 22 Jul 2002 11:12:01 GMT”>**

The date and time after which the document should be considered expired. An illegal EXPIRES date, e.g. “0”, is interpreted as “now”. Setting EXPIRES to 0 may thus be used to force a modification check at each visit.

Web robots may delete expired documents from a search engine, or schedule a revisit.

[HTTP 1.1 (RFC 2068)](http://www.w3.org/Protocols/rfc2068/rfc2068) specifies that all HTTP date/time stamps MUST be generated in Greenwich Mean Time (GMT) and in RFC 1123 format.

RFC 1123 format = wkday “,” SP date SP time SP “GMT”

wkday = (Mon, Tue, Wed, Thu, Fri, Sat, Sun)  
 date = 2DIGIT SP month SP 4DIGIT ; day month year (e.g., 02 Jun 1982)  
 time = 2DIGIT “:” 2DIGIT “:” 2DIGIT ; 00:00:00 – 23:59:59  
 month = (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec)

 

## Pragma NO-CACHE

**<META HTTP-EQUIV=”PRAGMA” CONTENT=”NO-CACHE”>**

This directive indicates cached information should not be used and instead requests should be forwarded to the origin server. This directive has the same semantics as the [CACHE-CONTROL:NO-CACHE](#cache-control) directive and is provided for backwards compatibility with HTTP/1.0.

Clients SHOULD include both PRAGMA:NO-CACHE and CACHE-CONTROL:NO-CACHE when a no-cache request is sent to a server not known to be HTTP/1.1 compliant.

### Additional Resources

- [So you don't want cache huh?](http://www.htmlgoodies.com/beyond/reference/article.php/3472881/So-You-Dont-Want-To-Cache-Huh.htm)
- [Useful HTML metatags](http://www.i18nguy.com/markup/metatags.html)
- What looks like the ultimate guide to website caching – [Caching Tutorial](http://www.mnot.net/cache_docs/) (Thanks Fotis for that link)

 