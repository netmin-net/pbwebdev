---
# http://learn.getgrav.org/content/headers
title: Adding Breadcrumb Microdata to Your Joomla Website
slug: adding-breadcrumb-microdata-to-your-joomla-website
# menu: Adding Breadcrumb Microdata to Your Joomla Website
date: 04-02-2014
published: true
publish_date: 04-02-2014
# unpublish_date: 04-02-2014
# template: false
# theme: false
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration-status: review
    category: [Search Engine Optimisation]
    tag: [Joomla,Microdata,SEO]
author: Peter Bui
metadata:
    author: Peter Bui
    description: Adding breadcrumb microdata to improve Google search results
    keywords: Joomla, microdata, breadcrumbs
    robots: index, follow
#      og:
#          title: The Rock
#          type: video.movie
#          url: http://www.imdb.com/title/tt0117500/
#          image: http://ia.media-imdb.com/images/rock.jpg
#  cache_enable: false
#  last_modified: true

---
Recently, we launched our [new portfolio site](https://pbwebdev.com/our-work "Our new portfolio website") and I personally have been tweaking parts of it as the days go by. I guess it is a little side project that I keep tapping away at and never will be finished.

One of the more interesting things in the new site build is the addition of microdata into the site. In particular breadcrumb microdata.

We've always used microdata in some way or form on our websites but it should be the norm and all websites. All websites should contain microdata if you care about search optimisation and how data is presented to the world.

In this screen capture we can see some terrible meta descriptions that have been set for the two search results, but highlighted in yellow, we can also see that the breadcrumbs of the website have been included in the search results. This is possible because of microdata.

This isn't new, in fact, Google has been using microdata and microformats since 2010. We've always had the our breadcrumbs in most if not all of our search results because of the way we structured and presented our data but this time we took it a little step further and made sure that our new Joomla site presented better and in the way that Google wants it to be displayed using microdata properly.

This [article from Google's help](https://support.google.com/webmasters/answer/185417 "Google article on implementing breadcrumb microdata") details how it can be implemented properly using microdata. It details how the code should be formatted and how each element in the code is marked up as various parts.

So what did we do? We implemented the microdata scheme into a HTML override for our template and will do also for all templates that we now produce so that our clients all have a slight competitive advantage in how their Joomla site is displayed on the search engines. At the moment we can't place this into the core of Joomla as it will potentially be overridden in a Joomla update.

Once the code has been implemented, you can actually test to see how the information will be displayed for Google to see and potentially be index as by using [Google's structured data testing tool](http://www.google.com/webmasters/tools/richsnippets?q=http%3A%2F%2Fpbwebdev.com%2Fwhat-we-do%2Fjoomla).

Google even takes this a step further by providing a Structured Data Markup Help tool to help web masters fill in the blanks around the structured data.

We've made our code public and you can access the HTML override on a GitHub repository.

It has been tested and implemented on Joomla 3 and will also be tested and implemented on Joomla 2.5.

We plan to keep the microdata overrides coming with more and more additions. I hope some of these tweaks and improvements can make their way into the Joomla! core to make Joomla even better than what it is now.

See our [follow up article](http://pbwebdev.com/blog/breadcrumb-microdata-override "Breadcrumb Microdata Override") on using the HTML override and the download link for the override. 