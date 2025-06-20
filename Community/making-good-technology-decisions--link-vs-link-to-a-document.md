---
title: Link vs News Link vs Link to a Document
ms.date: 06/18/2025
author: brianpmccullough
ms.author: 
ms.reviewer: 
manager: 
ms.topic: article
ms.service: SharePoint Online
ms.localizationpriority: Low
description: "Link vs News Link vs Link to a Document"
ms.collection:  SPCommunity
---

# Link vs News Link vs Link to a Document

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

There are many ways to link to web hosted content within SharePoint Online.  On pages you can use hyperlinks within Text web parts, and many other web parts such as Quick Links, Heros, Call to Action, etc.  In lists and libraries you can use Hyperlink columns within columns.  In addition, there are more specialized files or content types including the Link, News Link, and Link to a Document content type which will automatically redirect you to the target url.

Link, News Link, and Link to a Document are similar in capabilities, but also differ in some aspects.  This document outlines the similarities and differences to help you determine which option best meets your needs.

Throughout the document statements about the capabilities are discussed from a perspective of what's possible out of the box or with the user interface provided by SharePoint Online.  Some additional scenarios may be possible using code, scripts, and/or automations.

## Link

After creating a new SharePoint Online site, using either the modern Team or Communication templates, you have the ability to create a "Link" in document libraries.  This is available by default in any new library, including the "Site Pages" and "Documents" libraries you get when you initially create the site.  It's also available by default on any new library you add to your site.

When you create a Link from the menu, you are prompted to enter the url of the web page or document to which you want to link.  This link can be to another page or document in SharePoint Online or to any other web site.  Optionally, you can use a picker to choose from files in your tenant (e.g. recent files or files from a particular site/library).  See also: https://support.microsoft.com/en-us/office/add-a-link-in-a-document-library-346b1eb9-1e71-4155-80ca-f868d058a56a

![Creating a web link from Site Pages library'](media\making-good-technology-decisions--link-vs-link-to-a-document\Link-SitePages-Web.png)


![Creating a document link from a document library'](media\making-good-technology-decisions--link-vs-link-to-a-document\Link-Documents-CreateInternalLink.png)

Regardless of the type of library or method you use to create the Link, creating a Link results in a .url file being created.  A .url file is essentially a shortcut that, when opened, launches the url contained within the file. This is the behavior when it's clicked within a library view.  If a Link file is downloaded and opened, assuming you haven't changed your file extension mappings on your machine, it will also navigate you to the url.

The link to the content is not stored as metadata, but rather embedded within the .url file contents.  A .url file is just a special text file with the following format:

```
[InternetShortcut]
URL=https://www.example.com
```

When a Link is created, it is assigned the default content type of the library.  Without changes to a standard document library this would be "Document".  In a Site Pages library, this would be "Site Page".

![Creating a link where custom content types have been used'](media\making-good-technology-decisions--link-vs-link-to-a-document\Link-Document-ContentType.jpg)

You cannot alter the New Form for a "Link"; a Link is always created using the dialog (in a document libary) or panel (in Site Pages library).  Changing metadata associated with the Link, including it's content type, is done after it is created.

### Link in the Highlighted Content Web Part
The Link displays a generic browser graphic, rather than a preview of the document.  

The file name is used as the main text of the card.  If displaying Link files in Highlighted Content web parts is important in your scenario, care should be taken with the way SharePoint Online names the Link files.  It'll probably be important that content owners change the Name property to a more friendly name.

The Author and Date displayed are associated with the Link, not the original content in the case of linking to a separate page or file in SharePoint Online.

When filtering Highlighted Content web parts by content type, be sure to remember that by default, a Link is assigned the default content type of the library associated with it.

It's worth noting that, at least as of the last edit of this article, clicking a Link card within a Highlighted Content web part directs you view item page, which cannnot handle automatic redirect of the .url and requires additional user interaction.

![Clicking a Link from a Highlighted Content Web Part'](media\making-good-technology-decisions--link-vs-link-to-a-document\Link-Document-HighlightedContent.jpg)

### Link in Search Results
As in the Highlighted Content Web Part, Link files appear with a generic browser icon and display the .url filename as the title.

When clicked, from a search result, the Link also attempts to navigate the user to a view form, however it cannot be displayed.  The user can continue to the content by clicking the Open button.

![Clicking a Link from a Search Result'](media\making-good-technology-decisions--link-vs-link-to-a-document\Link-Search.jpg)

### Link in the News Web Part
Link files cannot be published (at least not without using script, code, or automation), as a result cannot be displayed in News web part.

## News Link
The News Link allows a content owner to link to another news page.  The linked url can be within SharePoint Online or any web address.  

While a News Link can link to any web address, News Links publish the linked document as "News" within SharePoint Online (i.e. sets it's Promoted State to 2). As a result News Link should be used for news scenarios, rather than general links.  This is a good choice, for example, to link to news from a company's public facing site, an industry news site, or from another site in SharePoint Online (e.g. regional news sites linking to corporate news or vice versa).

Creating a News Link is not available to content owners within the Site Pages library.  It is, instead, triggered from the home page of a modern SharePoint Online site using the New menu (or from a News web part using the "Add" menu).

![Creating a new News Link'](media\making-good-technology-decisions--link-vs-link-to-a-document\NewsLink-Create.jpg)

When creating a News Link, you provide a url to the web page.  Once provided, SharePoint Online will attempt to prepopulate the Preview Image, Title, and Description by reading the social metadata tags from the web page.  If no social metadata tags can be read, or if the content owner prefers to change them, these fields can be edited by the content owner.  See also: https://support.microsoft.com/en-us/office/create-and-share-news-on-your-sharepoint-sites-495f8f1a-3bef-4045-b33a-55e5abe7aed7#bkmk_newslink

Upon creation, you will get a published news article (i.e. Promoted State = 2).  Behind the scenes, SharePoint Online has created an .aspx file with a "Repost Page" content type.

![News Link as a Repost Page content type with Promoted State equal to 2'](media\making-good-technology-decisions--link-vs-link-to-a-document\NewsLink-PromotedState-ContentType.jpg)

It is worth noting that the "Repost Page" content type inherits from "Site Page", so any web parts or searches that pull in "Site Pages" (or any derivative of them), will work well with "Repost Page".  These work well with the News and Highlighted Content web parts for example.  Unlike the Link files, when clicked in these web parts, the user is redirected without an intermediate "viewer" page.

![News Link in web parts'](media\making-good-technology-decisions--link-vs-link-to-a-document\NewsLink-WebParts.jpg)

There is not an out of the box way to have a News Link (aka Repost Page) to not be treated as news.  However, code, scripts, listview formatting, or automations can be used to change the Promoted State from "2" to "0" which will prevent it from treated as News.

While the Repost Page content type can be added to other libraries, there is not an ability to get items in the library associated with this content type.  

As a result, News Link is really only practical for use with news content within the Site Pages library.

## Link to a Document
If you have only ever used SharePoint Online with modern team or communication sites, you may not even be familiar with the "Link to a Document" content type.  They provide similar capabilities as the Link (.url files) and News Link (i.e. Repost Page content type) mentioned above.

To use a "Link to a Document", you must add the "Link to a Document" content type (or a content type which inherits from the "Link to a Document") to your library.

![Adding Link to a Document to a library'](media\making-good-technology-decisions--link-vs-link-to-a-document\LinkToADocument-AddToLibrary.jpg)

Once added as a content type to the library, you can create a "Link to a Document" by using the "New" menu within the library.

![New Link to a Document'](media\making-good-technology-decisions--link-vs-link-to-a-document\LinkToADocument-New.jpg)

You are prompted to enter the Name and Url to the page or document.  Note this can be an internal or external link.

![New Form for Link to a Document'](media\making-good-technology-decisions--link-vs-link-to-a-document\LinkToADocument-NewForm.jpg)

Note that even if you've created a custom Link to a Document content type with additional metadata, you initially only set the Name and Url. If additional metadata is specified for your Link to a Document based content type, this can be edited after specifying the Name and Url.

![New Form for Link to a Document with custom properties'](media\making-good-technology-decisions--link-vs-link-to-a-document\LinkToADocument-NewFormCustomProperties.jpg)

Also note the Link to a Document is always created as an .aspx file.  Unlike the Link (and associated .url files) the .aspx files are a proprietary form of a redirect and can only be interpreted by SharePoint Online.  You cannot, for example, download the .aspx file and expect the shortcut/link to work on your desktop.  In addition, it might be a bit awkward to have .aspx files in document libraries given this is the extension associated with Site Pages.

![Link to a Document as an aspx file'](media\making-good-technology-decisions--link-vs-link-to-a-document\LinkToADocument-ASPX.jpg)

Interestingly, Link to a Document is not shown with the default configuration of Source : This Site and Type : Documents.  You must change to the particular library, or change Type to all, or otherwise filter based on managed properties.

![Link to a Document in Highlighted Content Web Part'](media\making-good-technology-decisions--link-vs-link-to-a-document\LinkToADocument-HighlightedContentWebPart.jpg)

When Link to a Documents are displayed in Search, they display the document name as specified when created.  In addition, they are immediately and successfully redirected to the page or document.

![Link to a Document in search results'](media\making-good-technology-decisions--link-vs-link-to-a-document\LinkToADocument-SearchResults.jpg)

---

**Principal author** [Brian P. McCullough](https://www.linkedin.com/in/brianpmccullough/)

I invite authors with their knowledge on this topic to contribute to this article, sharing their experience.

---
