---
# http://learn.getgrav.org/content/headers
title: SobiPro Documentation &#038; Coding Cheat Sheet
slug: sobipro-documentation-coding-cheat-sheet
# menu: SobiPro Documentation &#038; Coding Cheat Sheet
date: 17-05-2015
published: true
publish_date: 17-05-2015
# unpublish_date: 17-05-2015
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

This post contains the standard methods for displaying information from fields created in SobiPro.

## Different Layouts

There are two main different layouts that you will be editing in SobiPro to display your information, vCard on the category or section view, and entries which is the full detailed view of a listings.

Fields on either of these views can be controlled and displayed according to how a designer or developer wishes.

### vCard

The vCard is the layout that you will be editing for the category list view. In regular Joomla!, this is the listings within a category.

Usually found in your Sobi template directory under /templates/templatename/common/vdard.xsl

### Entires

Entries are the full detailed view of a listing. This usually has all the fields that a user might set up in the admin area of SobiPro.

## Code Samples for Different Parts of SobiPro vCard and Entry Views

### Displaying an Entry Title with Link on a SobiPro vCard view

The title of an entry is usually the most common field that is displayed. The code below will show the title in a heading 1 tag and also includes the URL to the entry full view.

 
    <pre style="padding-left: 30px;"><h1>
     <a href="{url}"><xsl:value-of select="name" /></a>
     </h1>

### Displaying Read More Button on SobiPro vCard view

This read more text will use the standard Bootstrap class btn to display a button link to the entry.

 
    <a class="btn" href="{url}" >Insert your read more text here</a>

### Adding Condition IF Statements to vCard or Entry View

From time to time you will need to add conditional statements into the XSL files and a condition such as view only if logged in or registered users only is a good example.

This condition allows a registered user with an valid user ID to view the link to read more.

The first line test if the user has an ID number or not. A logged in user will have a user ID. A user that is not logged in, will have an ID of 0.

 
    <pre style="padding-left: 30px;"><strong><xsl:if test="//visitor/@id > 0"></strong>
     <p>
     <a class="btn" href="{url}" >Read more</a>
     </p>
     <strong></xsl:if></strong>

If the user's ID equals 0, then the user doesn't have an account with the website and will be prompted to register to gain access to the website.

 
    <pre style="padding-left: 30px;"><strong><xsl:if test="//visitor/@id = 0"></strong>
     <p>
     <a class="btn" href="index.php?option=com_users" >Register to Read More</a>
     </p>
     <strong></xsl:if></strong>

The key thing in this statement is the test of the visitor's ID

 
    <pre style="padding-left: 30px;"><strong>test="//visitor/@id = 0"</strong>

### **Conditional Publish Statement**

If you need to check if a value meets a condition for publishing, this is how you do it.

**vCard View**

 
      <xsl:if test="fields/FIELDNAME/data = 'VALUE'">
        <xsl:value-of select="fields/FIELDNAME/data" />
      </xsl:if>

**Details View**

 
      <xsl:if test="entry/fields/FIELDNAME/data = 'VALUE'">
        <xsl:value-of select="entry/fields/FIELDNAME/data" />
      </xsl:if>

### Display Categories that an Entry Belongs To

This code for an entry view will display the categories of an entry depending in if it has categories or not. First testing the case if the entry has categories, and then loading each category and its URL to link to the category.

 
    <xsl:if test="count(entry/categories)">
     <div class="spEntryCats">
     <xsl:value-of select="php:function( 'SobiPro::Txt' , 'ENTRY_LOCATED_IN' )" /><xsl:text> </xsl:text>
     <xsl:for-each select="entry/categories/category">
     <a href="{@url}">
     <xsl:value-of select="." />
     </a>
     <xsl:if test="position() != last()">
     <xsl:text> | </xsl:text>
     </xsl:if>
     </xsl:for-each>
     </div>
     </xsl:if>

### 

### Displaying Fields with HTML Formatting

Some fields that you create in SobiPro may be set to have the WYSIWYG editor on them and in turn there will be HTML in the output of the field. To make this display correctly you will have to enable “**disable-output-escaping**” and set it to yes so that the HTML will render properly.

**HTML rendering in vCard view**

 
     <xsl:value-of select="fields/FIELDNAME/data" disable-output-escaping="<strong>yes</strong>" />

**HTML rendering in Entry view**

 
     <xsl:value-of select="entry/fields/FIELDNAME/data" disable-output-escaping="<strong>yes</strong>" />

### Displaying Images in Details View

 
    <div class="pull-right">
     <img class="spFieldsData" width="100px">
     <xsl:attribute name="title">
     <xsl:value-of select="entry/FIELD_NAME" />
     </xsl:attribute>
     <xsl:attribute name="alt">
     <xsl:value-of select="entry/FIELD_NAME" />
     </xsl:attribute>
     <xsl:attribute name="src">
     <xsl:value-of select="entry/fields/FIELD_IMAGE/data/img/@src" />
     </xsl:attribute>
     </img>
     </div>

### Displaying the Categories an Entry Belongs To

 
    <div class="category-list">
     <xsl:if test="count(entry/categories)">
     <div class="spEntryCats">
     <xsl:value-of select="php:function( 'SobiPro::Txt' , 'Categorised in:' )" /><xsl:text> </xsl:text>
     <xsl:for-each select="entry/categories/category">
     <a>
     <xsl:attribute name="href">
     <xsl:value-of select="@url" />
     </xsl:attribute>
     <xsl:value-of select="." />
     </a>
     <xsl:if test="position() != last()">
     <xsl:text> | </xsl:text>
     </xsl:if>
     </xsl:for-each>
     </div>
     </xsl:if>
     </div>

 

### Links within XSL

It is important to note that links in the layouts need to be encoded. For example:

 
    index.php?option=com_users<strong>&</strong>view=registration

In this example, the **& **in the URL will break the XSL layouts. It is important to encode the characters and convert **&** into **&** in order to render correctly.

 