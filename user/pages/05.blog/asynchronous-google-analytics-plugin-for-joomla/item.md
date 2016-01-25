---
# http://learn.getgrav.org/content/headers
title: Asynchronous &#038; Universal Google Analytics Plugin for Joomla
slug: asynchronous-google-analytics-plugin-for-joomla
# menu: Asynchronous &#038; Universal Google Analytics Plugin for Joomla
date: 19-04-2010
published: true
publish_date: 19-04-2010
# unpublish_date: 19-04-2010
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
    tag: [Google,Joomla,Plug-in,Google,Joomla,Plug-in]
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

[![google-analytics](https://nicheextensions.com/images/extensions/google-analytics.png)](https://nicheextensions.com/extensions/google-analytics)Normally we would embed the Google Analytics tracking code in to the template of each of the sites that we are build. In some circumstances we'd find that the end user would want more control over the Google Analytics code and would prefer to switch it on and off or insert new tracking code at their own will. So we've compiled this little plugin that allows for just that. Loading the Google Analytics code asynchronously allows for the rest of your site to load while the analytics code loads in the background and thus increasing the loading speed of your site by a few seconds. Since Google now actively looks at your websites loading performance to calculates its search engine rankings, this plug-in is well worth a try.

This plugin now has a [pro version](https://nicheextensions.com/extensions/google-analytics "Google Analytics Pro for Joomla") that allows you to fine tune your Google Analytics configuration.

This plug-in allows you to simple add in the web property ID supplied by Google in your analytic account in to its parameters. (e.g. UA-XXXXX-X).

Find out how to identify your [web property ID](#webProperty "Finding Google Web Property ID").

**It does not track the administrator area of your site** and embeds the required Javascript the way that Google recommends, just before the closing  tag. Simple install the plug-in, add in the tracking code in to the parameters and enable the plug-in.

To read more about the asynchronous method of embedding Google Analytics please refer to the Google [documentation](https://developers.google.com/analytics/devguides/collection/gajs/asyncTracking).

### Version 3.0

We've gone simple. This new version of the Google Analytics plugin has now gone simple!

We'll be releasing a pro version soon that will have all of the advanced features. Of course you can still download the older version in the 2.5.7 series to get some of those advanced feature but all the new goodies will be in version 3.

Version 3 has been updated to work with an auto updater and also with the web installer found in Joomla 3.2.

You can [download version 3.0](http://nicheextensions.com/extensions/google-analytics) now ready for Joomla 3 and Joomla 2.5.

- <https://nicheextensions.com/extensions/google-analytics>

 

### After all the advanced features? Go Pro!

If you're after all the advanced features where you can fine tune how Google Analytics works, the subscribe for a PRO subscription to the plugin for only $4.95 (Less than a beer in many countires).

- [ ](http://nicheextensions.com/extensions/google-analytics)<https://nicheextensions.com/extensions/google-analytics>[  
](http://nicheextensions.com/downloads/google-analytics-joomla)

 

## Older Versions

For the latest updates check the Niche Extensions website.

 

### Version 2.5.6 – 1st August 2012 Two new features

Added new features:

- Anonymous IP tracking to comply with German privacy laws
- Option to place code output at the end of the  output or at the bottom of the page before the closing  tag.

### Version 2.5.5 – 1st August 2012 No more new updates for J1.5

I'm going to stop updating the Joomla 1.5 version from here on in. As Joomla 1.5 is coming to end of life in September I won't be developing for it anymore. The Joomla 1.5 version will still be downloadable as is for usage but won't have any more new features.

### Version 2.5.4 – 16th Feb 2012 Bug Fixes

Bug fixed with sample rate overriding site speed variable. Also note that site speed has a max value of 10.

### Version 2.5.3 – 15th Feb 2012 New Advanced Features

- **Subdomain and Multiple top level domains** New support has been added to the plugin. It now supports multiple sub domains and multiple top level domains. e.g. example.com.au, example.com, example.co.uk
- **Sample rate specifications** Session timeout is used to compute visits, since a visit ends after 30 minutes of browser inactivity or upon browser exit. If you want to change the definition of a ‘session' for your particular needs, you can pass in the number of milliseconds to define a new value. This will impact the Visits reports in every section where the number of visits are calculated, and where visits are used in computing other values. For example, the number of visits will increase if you shorten the session timeout, and will decrease if you increase the session timeout. You can change the expiration timeout to 0 to indicate that this cookie should be deleted when the browser is closed.
- **Site speed sample rate specification** Maximum setting of 10. By default, a fixed 1% sampling of your site visitors make up the data pool from which the Site Speed metrics are derived. If you have a relatively small number of daily visitors to your site, such as 100,000 or fewer, you might want to adjust the sampling to a larger rate. This will provide increased granularity for page load time and other Site Speed metrics.
- **Visitor cookie timeout** Sets the Google Analytics visitor cookie expiration in milliseconds. By default, the visitor cookie is set to expire in 2 years. If you prefer, you can change the expiration date of the visitor cookie using this method. You can change the expiration timeout to 0 to indicate that this cookie should be deleted when the browser is closed.
- **Social Media Tracking** Allowing for the tracking of Facebook ‘like' and ‘unlikes' as well as Twitter actions for websites that have Facebook and Twitter integrated into their templates or website.
- **Tracking Differentiation Between Front End Logged in User and Frontend Visitor** Adding in the extra code required to track website members actions compared to that of website visitors.
- **Google Webmaster tools domain verification**

### Version 2.5.2 – 9th Feb 2012 – New Features – Multi Tracking

Addition of multi top level domain tracking and addition of multi sub domain tracking.

### Version 2.5.1 – 8th Feb 2012 – Update for Joomla 2.5

Updated the plugin to work with Joomla 1.5 – 2.5. Changed the versioning to match the latest Joomla version as well.

## Download the Plug-In

![Niche Extensions](http://nicheextensions.com/assets/niche-extensions-logo.png)Download from Niche Extensions



**Please make sure you download and install the right version for your Joomla instance **as installing the J1.5 version on J1.6 / J1.7 will break your site.

- ******Download the plug-in for  Joomla 1.6.x – 3.0.x: [plg\_AsynGoogleAnalytics-j25](https://nicheextensions.com/extensions/google-analytics) (j1.6.x-j3.0.x) (ZIP 3.84kb)**

- **Download the plug-in for  Joomla 1.5 ONLY: [plg\_AsynGoogleAnalytics](/images/blog/2010/04/plg_AsynGoogleAnalytics1.zip "Asynchronous Google Analytics for Joomla 1.5.x") (J1.5) (ZIP 3.3kb) No future updates**

 

If you use this plugin, leave a comment and please post a rating and a review at the [Joomla! Extensions Directory](http://extensions.joomla.org/extensions/site-management/site-analytics/12241 "link to Asynchronous Google Analytics plug-in on the Joomla Extension Directory").

 

 