---
# http://learn.getgrav.org/content/headers
title: Joomla 1.5.17 Update Released
slug: joomla-1-5-17-update-released
# menu: Joomla 1.5.17 Update Released
date: 28-04-2010
published: true
publish_date: 28-04-2010
# unpublish_date: 28-04-2010
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
    tag: [Joomla,Updates,Joomla,Updates]
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

Please when upgrading, make sure you do a test upgrade first in case some of your third party extensions break in the process. The Joomla Project announces the immediate availability of Joomla 1.5.17 [Wojmamni ama woobusani].

This is a priority release to correct two issues in version 1.5.16. Although there are no security issues fixed in this release, we consider it a security release because a security-related bug has been fixed and because many sites may be upgraded directly from 1.5.15 to 1.5.17.

The [Development Working Group's](http://docs.joomla.org/Development_Working_Group) goal is to continue to provide regular, frequent updates to the Joomla community.

## Download

- [Click here to download Joomla 1.5.17 (Full package) ¬ª](http://joomlacode.org/gf/download/frsrelease/12193/49624/Joomla_1.5.17-Stable-Full_Package.zip)
- [Click here to download Joomla 1.5.17 (Upgrade packages) ¬ª](http://joomlacode.org/gf/project/joomla/frs/?action=FrsReleaseBrowse&frs_package_id=5194)

## Updates and Fixes in This Release

### **Language **

- Updated ru-RU installation language ([20239)](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=20239)
- Added en-AU installation language ([20220)](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=20220)
- Updated help sites list ([20238)](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=20238)

### **System **

- Fixed problem logging in when Session Handler is set to None ([20221](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=20221))
- Fixed error message when running Joomla! in a PHP version prior to version 5.2 ([20219](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=20219))
- Reverted change to JFolder::makesafe method that introduced a bug ([16506](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=16506))

Statistics for the 1.5.17 release period:

- Joomla 1.5.17 contains: - 6 issues fixed in SVN
- 6 commits
- Tracker activity resulted in a net increase of 4 active issues: - 10 new reports
- 0 closed
- 6 fixed in SVN
- At the time the 1.5.17 release was packaged, the tracker had 307 active issues: - 171 open
- 105 confirmed
- 31 pending