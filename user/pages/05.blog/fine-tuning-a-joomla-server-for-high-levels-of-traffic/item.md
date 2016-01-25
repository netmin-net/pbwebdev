---
# http://learn.getgrav.org/content/headers
title: Fine Tuning a Joomla Server for High Levels of Traffic
slug: fine-tuning-a-joomla-server-for-high-levels-of-traffic
# menu: Fine Tuning a Joomla Server for High Levels of Traffic
date: 11-11-2009
published: true
publish_date: 11-11-2009
# unpublish_date: 11-11-2009
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

[![Web Server](wp-content/uploads/2009/11/Picture-1.png "Web Server")](wp-content/uploads/2009/11/Picture-1.png) We've recently been managing a website with a very high volume of traffic. Not only are there a huge amount of visitors but also a rather long stay time and usage or resources on the server. We investigated ways of optimizing the server and site to handle these high levels of traffic.

This particular Joomla based site averages roughly, 6000 unique visitors a day with user registering on the site every few minutes to interact with the site's functions.

So here are a few tips and tricks that can be done to optimise the server environment to help handle the high server loads after you have optimised your instance of Joomla. I must also add that these tweaks are for an Apache based web server.

### 1) Modify the Server KeepAlive settings.

**`KeepAlive`**

The Keep-Alive extension to HTTP/1.0 and the persistent connection feature of HTTP/1.1 provide long-lived HTTP sessions which allow multiple requests to be sent over the same TCP connection. In some cases this has been shown to result in an almost 50% speedup in latency times for HTML documents with many images. To enable Keep-Alive connections, set `KeepAlive On`.

**`KeepAliveTimeout`**

The number of seconds Apache will wait for a subsequent request before closing the connection. Once a request has been received, the timeout value specified by the `Timeout` directive applies.

Setting `KeepAliveTimeout` to a high value may cause performance problems in heavily loaded servers. The higher the timeout, the more server processes will be kept occupied waiting on connections with idle clients. Setting the timeout period too high may impact performance on high-traffic servers because the number of open TCP/IP connections can grow very large.

We recommend having the KeepAlive setting On and the KeepAliveTimeout setting as low as 1-2 seconds.

In our situation where multiple images, and MySQL requests where being made, we found that this dramatically increased the speed for the end user and also decreased server CPU usage.

**MaxKeepAliveRequests**

MaxKeepAliveRequests defines the maximum number of requests that may be serviced using a single TCP/IP connection. This is only relative if KeepAlive is On. It is also important to set a reasonable limit on this to help reduce the impact of some denial of service attacks on the server.

If may take a little bit of tweaking and testing to get the right amount for the MaxKeepAliveRequests for your server environment.

### Results

Immediately after changing a few of these settings on the server the site's load time had dramatically increased as well as reducing the server loads.

### Resources and Links

- [http://httpd.apache.org/docs/2.0/mod/core.html#maxkeepaliverequests](# http://httpd.apache.org/docs/2.0/mod/core.html#maxkeepaliverequests)
- [http://httpd.apache.org/docs/2.0/misc/perf-tuning.html](# http://httpd.apache.org/docs/2.0/misc/perf-tuning.html)
- [http://forum.whmdestek.com/site-server-administration/815-optimize-high-traffic-servers.html](# http://forum.whmdestek.com/site-server-administration/815-optimize-high-traffic-servers.html)
- [http://www.appwebserver.org/products/appweb/doc/guide/appweb/users/dir/perf.html](# http://www.appwebserver.org/products/appweb/doc/guide/appweb/users/dir/perf.html)