---
# http://learn.getgrav.org/content/headers
title: Joomla Update Version 1.5.16 Released
slug: joomla-update-version-1-5-16-released
# menu: Joomla Update Version 1.5.16 Released
date: 25-04-2010
published: true
publish_date: 25-04-2010
# unpublish_date: 25-04-2010
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

![Joomla 1.5.16](/wp-content/uploads/2010/04/joomla-1.5.16.png "Joomla 1.5.16")The latest update from Joomla has been released with a list of new patches and fixes to the Joomla core.

These changes include:

### Security

Four security issues were fixed in this release:

- Moderate Priority – Core – Negative Values for Limit and Offset. [More information](http://developer.joomla.org/security/news/311-20100423-core-negative-values-for-limit-and-offset.html)
- Low Priority – Core – Installer Migration Script. [More information](http://developer.joomla.org/security/news/310-20100423-core-installer-migration-script.html)
- Moderate Priority – Core – Sessation Fixation. [More information](http://developer.joomla.org/security/news/309-20100423-core-sessation-fixation.html)
- Low Priority – Core – Password Reset Tokens. [More information](http://developer.joomla.org/security/news/308-20100423-core-password-reset-tokens.html)

For additional information, visit the [Joomla Security Center](http://developer.joomla.org/security.html).

### **Components**

- Fixed error in contacts with SEF enabled ([17235](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=17235))
- Fixed SQL error when sorting news feeds by section. ([18648](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18648))
- Fixed problem showing URL for image files in Atom news feeds. ([18936](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18936))
- Fixed problem where author alias was not escaped correctly. ([19009](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19009))
- Fixed bug in pagination of category blog menu item. ([19245](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19245))
- Fixed display of image captions in some situations. ([19405](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19405))
- Fixed caching problem with com\_contact. ([19435](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19435))
- Added framework validation to com\_media file. ([19763](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19763))
- Fixed PHP notice when enabling or disabling a user. ([19798](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19798))

### **Modules**

- Fixed caching for related articles module ([17000](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=17000))
- Fixed notification error in login module ([17762](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=17762))
- Fixed problems with upgrade method in module installation ([17878](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=17878))
- Fixed typo in mod\_latestnews. ([18403](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18403))
- Fixed HTML validation problem with mod\_search. ([18619](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18619))
- Fixed problem with some news feeds not showing. ([18672](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18672))
- Fixed problem in mod\_login where trashed menu items show in redirect list. ([19831](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19831))

### **Plugins **

- Fixed problem saving content in TinyMCE when editor is toggled ([17936](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=17936))
- Fixed bug in email cloaking that added an extra space ([17986](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=17986))
- Fixed problem saving valid attributes for some HTML tags. ([19055](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19055))

### **Legacy **

- No legacy issues were fixed for this release

### **Templates **

- Fixed problem loading template files for RTL languages. ([18614](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18614))
- Fixed beez template to show correct Itemid after a search. ([18683](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18683))

### **Language **

- Added missing translation strings in installation. ([19604](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19604))
- Added sr-YU language for installation. ([19627](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19627))
- Added Phnom-Penh to timezone files. ([19715](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19715))
- Added missing language strings in installation files. ([19816](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19816))
- Added Arabic Unitag installation language ar\_AA ([19836](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19836))
- Added missing language strings for is-IS language in installation. ([19864](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19864))
- Added missing strings in installation ini files. ([19871](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19871))
- Added new hi-IN install language ([19966](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19966))
- Added updates on installation ini files ([20024](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=20024))
- Fixed language bug in Menus ([20055](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=20055))
- Added language credits update ([20195](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=20195))

### **Administrator **

- Fixed display problem in back end with RTL languages. ([18570](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18570))
- Fixed problem where Menu Item types for disabled components still showed when adding menu items. ([18617](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18617))
- Fixed problem with display of module position in Module Manager. ([18848](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18848))

### **System **

- Fixed JFolder::makeSafe method to not remove dots in path ([16506](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=16506))
- Fixed problem that prevented using a cache in some cases ([16974](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=16974))
- Remove PHP warning message on some versions ([18612](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18612))
- Fixed problem installing modules in update mode. ([18987](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18987))
- Fixed problem with Yagoon and Norfolk timezones. ([19555](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19555))
- Fixed problem with return value when saving polling components. ([19655](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19655))
- Fixed problem in JToolbarHelper class media\_manager method. ([19680](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19680))
- Fixed incorrect URI for IIS platforms ([18046](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=18046))
- Improved handling of failing Apache plugins ([19859](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=19859))
- Added Reykjavik in timezone ([20025](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=20025))
- Fixed JApplication::redirect() to not use 301 code ([20043](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=20043))
- Fixed SEF search URL's for cross-platform compatibility ([20184](http://joomlacode.org/gf/project/joomla/tracker/?action=TrackerItemEdit&tracker_item_id=20184))

Statistics for the 1.5.16 release period:

- Joomla 1.5.16 contains: - 48 issues fixed in SVN
- 52 commits
- Tracker activity resulted in a net increase of 83 active issues: - 224 new reports
- 94 closed
- 48 fixed in SVN
- At the time the 1.5.16 release was packaged, the tracker had 303 active issues: - 169 open
- 103 confirmed
- 31 pending

## What Does This Mean For You

Check to see if the updates and changes will effect you or if you need them straight away. All major security updates from Joomla should always be applied straight away. Get your site ready in a test environment and update your test Joomla site to the latest version.

Check that all of your extensions are working properly and then roll out the changes to your live environment. If there are issues with your site and other extensions then it might be worth waiting for your extension developers to patch and update their extensions to work with any of the changes in Joomla 1.5.16 before upgrading and breaking your site.

Download the latest updates from the [Joomla Downloads page](http://www.joomla.org/download.html).

Have you seen some of our new [nifty little extensions](http://extensions.joomla.org/extensions/owner/buipy001%40gmail-2Ecom) on the extensions directory yet?

*PB Web Development is not affiliated with or endorsed by the Joomla Project or Open Source Matters. The Joomla logo is used under a limited license granted by Open Source Matters the trademark holder in the United States and other countries.*