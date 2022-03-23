---
title: Query String URL Tricks for SharePoint & M365
ms.date: 03/22/2022
author: PatD
manager: 
ms.topic: article
ms.author: 
ms.service: sharepoint-online
localization_priority:
description: Creative ways to filter, embed, and change page content by learning the secrets of URL query strings.
ms.collection: M365Community
---
  
# Query String URL Tricks for SharePoint & M365

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

The stoic URL is a core tenant of our online lives. Despite all the apps, browsers, and tools that obfuscate it, behind the scenes it is all glued together by the Uniform Resource Locator (URL). The data that populates the Teams app on your phone wouldn't make it there without the URL of the Graph API endpoint.

As a site owner, you'll see URLs all the time – SharePoint sites, Microsoft Forms, shared links. This article will cover a few parameters you can stick on the end of a URL to make your job easier, and to give you more options in solving problems.

## The thing about query strings is… they are everywhere

You know this URL brings you to a website:

```html
https://docs.microsoft.com
```

And this one brings you to a specific _section_ of that same website:

``` html
https://docs.microsoft.com/en-us/search/
```

What about this URL?

```html
https://docs.microsoft.com/en-us/search/?terms=community%20content
```

It has a **?** at the and with a key (_term_) and a value (_community content_). This is a **URL query string.** Based on the key and value in it, it filters or updates the page to show different content.

You can change the value (try _document sets_) and the page content is different. You did all the filtering in the address bar of the browser:

```html
https://docs.microsoft.com/en-us/search/?terms=document%20sets
```

Here's an example of multiple filtering with two keys (_products_ and _languages_) with their corresponding values (_m365_ and _javascript):_

[<https://docs.microsoft.com/en-us/samples/browse/>

](<https://docs.microsoft.com/en-us/samples/browse/>)[https://docs.microsoft.com/en-us/samples/browse/?products=m365&amp;languages=javascript](https://docs.microsoft.com/en-us/samples/browse/?products=m365&amp;languages=javascript)

This same page loads different content with different values (_ms-graph_ and _html_)
[https://docs.microsoft.com/en-us/samples/browse/?products=ms-graph&amp;languages=html](https://docs.microsoft.com/en-us/samples/browse/?products=ms-graph&amp;languages=html)

How does this mental modal of URL-as-page-transformer work in Microsoft 365? Keep reading!

### Put a Modern SharePoint page into Edit mode

Any Modern SharePoint Online page can be placed into **Edit** Mode by adding this query string URL: ?Mode=Edit

https://\&lt;yoursite\&gt;.sharepoint.com/sites/\&lt;sitename\&gt;/SitePages/default.aspx

https://\&lt;yoursite\&gt;.sharepoint.com/sites/\&lt;sitename\&gt;/SitePages/default.aspx?Mode=Edit

This isn't really _easier_ than clicking the button on the page, but it's a good example of changing a page's look or function dramatically with a URL query string.

The spaces in-between

The URL, like the one in your browser's address bar right now, usually support spaces. So something like ?terms=policy security works just fine. Where it doesn't work is when you share the URL via Email, text or Teams by copying and pasting it. As a best practice, replace any space in your URL query string with a %20, like ?terms=policy%20security.

### Put a Modern SharePoint page into Maintenance mode

Any Modern SharePoint Online page, like:

https://\&lt;yoursite\&gt;.sharepoint.com/sites/\&lt;sitename\&gt;/SitePages/default.aspx

 … can be placed into _Maintenance Mode_ by adding this URL query string: ?maintenancemode=true

https://\&lt;yoursite\&gt;.sharepoint.com/sites/\&lt;sitename\&gt;/SitePages/default.aspx?maintenancemode=true

 This gives you a behind-the-scenes view of the web parts on the page, and the data being sent back and forth between the page and the browser. This tool is helpful for diagnosing issues with pages including those using the SharePoint Framework (SPFX).

Read the official documentation on this here: [https://docs.microsoft.com/sharepoint/dev/general-development/client-side-web-parts-maintenance-mode](https://docs.microsoft.com/sharepoint/dev/general-development/client-side-web-parts-maintenance-mode)

### Put (nearly) anything SharePoint into a focused mode

In the _Classic_ SharePoint days, there was a way to create a focused view of just content by appending _isDLg=1_ as a URL query string. Those days are in the rearview, but there's an updated version for Modern SharePoint

**?env=Embedded**

This hides the main navigation, side navigation (and App bar) on just about anything in your SharePoint site, including:

- Pages
- List views
- Site Contents
- Site Analytics
- Recycle Bin

For example in a list it would be:
https://\&lt;yoursite\&gt;.sharepoint.com/sites/\&lt;sitename\&gt;/Lists/\&lt;yourlistname\&gt;/allitems.aspx?env=Embedded

In a page it would be:
https://\&lt;yoursite\&gt;.sharepoint.com/sites/\&lt;sitename\&gt;/SitePages/default.aspx?env=Embedded

### Make any SharePoint List into a _Microsoft Lists_ list

If you've been building in Microsoft 365 for a while, you're probably used to working in SharePoint sites with pages, web parts, workflows, and navigations. Sometimes you just want to share the context of a single list or library within that site – and with a URL query string you can do just that.

Take your list, remove any existing query string content on the end down to this:

 https://\&lt;yoursite\&gt;.sharepoint.com/sites/\&lt;sitename\&gt;/Lists/\&lt;yourlistname\&gt;/allitems.aspx

 … and append this to the end:

?env=WebViewList

Like this:
 https://\&lt;yoursite\&gt;.sharepoint.com/sites/\&lt;sitename\&gt;/Lists/\&lt;yourlistname\&gt;/allitems.aspx?env=WebViewList

That's it! Now your SharePoint list displays in Microsoft Lists. This is a great way to maximize screen real estate and help focus people during collaboration. This list remains housed in its SharePoint site, but now with all the user interface polish of Microsoft Lists.

Filter, and filter some more

Sometimes you need to apply two URL query string filters to the same URL – two keys and two values. The format for that is generally to use the question mark first, and the ampersand for every additional key/value pair, like:

page.aspx?mykey=myvalue&amp;thisotherkey=someothervalue

### Create a link to a List or Library Search Result

Within the Modern user interface, the search bar sets its context (or scope) to the List or Library you're in. When you perform a search, it appends a URL query string filter of the results.

 Here's my list:

https://\&lt;greatsharepointsite\&gt;.sharepoint.com/sites/Lists/\&lt;ListName\&gt;/AllItems.aspx

Here it is after a search for the phrase _tax documents_:

https://\&lt;greatsharepointsite\&gt;.sharepoint.com/sites/Lists/\&lt;ListName\&gt;/AllItems.aspx?view=7&amp;q=tax%20documents

And if you change the value of the _q_ key in the URL query string, the page will change:

 https://\&lt;greatsharepointsite\&gt;.sharepoint.com/sites/Lists/\&lt;ListName\&gt;/AllItems.aspx?view=7&amp;q=consultants

You can share this link, in a way that works almost like a SharePoint view.

 Kick things up a notch by also adding the focused-mode query string filter in combination, like:

https://\&lt;greatsharepointsite\&gt;.sharepoint.com/sites/Lists/\&lt;ListName\&gt;/AllItems.aspx?view=7&amp;q=engineering&amp;env=Embedded

###

### Debug SharePoint Framework Webparts and Extensions

You can troubleshoot a SharePoint page to see if there is a SharePoint Framework (SPFx) extension or web part causing trouble. Add this ?disable3PCode=1 to the URL to disable loading of anything SPFx:

https://\&lt;yoursite\&gt;.sharepoint.com/sites/\&lt;sitename\&gt;/SitePages/default.aspx?disable3PCode=1

Read the official documentation on this: [https://docs.microsoft.com/sharepoint/dev/general-development/client-side-web-parts-maintenance-mode#disable-spfx-web-parts-and-extensions](https://docs.microsoft.com/sharepoint/dev/general-development/client-side-web-parts-maintenance-mode#disable-spfx-web-parts-and-extensions)

###

 Filter Lists &amp; Library Views in SharePoint and Microsoft Lists

SharePoint Lists and Libraries let you filter by specific column values with a URL query string. This might let you have a URL that filters a status column, or shows only items where some value is true.

A use-case might be using Power Automate Flow to Email a list view status report based on a given product in a list… with hundreds of possible products. You don't want to make separate Views for each product. So, you make a single view and use URL query strings to create dynamic URLs for your Flow

The basic syntax for this is:

?useFiltersInViewXml=1&amp;FilterField1 **=\&lt;internalFieldName\&gt;** &amp;FilterValue1= **\&lt;value\&gt;**

- The FilterField key needs to be the internal name of the SharePoint column. If you rename 'Title' to 'Product' in your list, you'll need to use 'Title' in your query string URL.

 You can find out the internal name by going to List Settings, choosing the column, and looking after the &amp;Field= key in the URL.

- When filtering yes/no columns, replace &quot;no&quot; with 0 and &quot;yes&quot; with 1 in your URL query string.

- Filtering like this (with the URL query string) means never having to wait for search. SharePoint Search can sometimes take a few minutes to pick up on a change, but this filtering is immediate.

- You can filter by multiple keys/values by incrementing the numbers, like this:
?useFiltersInViewXml=1&amp;FilterField1=[internalFieldName]&amp;FilterValue1=[value]&amp;FilterField2=[internalFieldName2]&amp;FilterValue2=[value]&amp;FilterField3=[internalFieldName3]&amp;FilterValue3=[value]

Further reading on the subject:

- Nate Chamberlain: [https://natechamberlain.com/2020/05/09/how-to-filter-a-sharepoint-list-or-library-using-url-parameters/](https://natechamberlain.com/2020/05/09/how-to-filter-a-sharepoint-list-or-library-using-url-parameters/)

- Piyush K Singh: [https://piyushksingh.com/2019/05/24/generate-modern-list-filter-url-managed-metadata/](https://piyushksingh.com/2019/05/24/generate-modern-list-filter-url-managed-metadata/)

---

**Principal author**: [Patrick M. Doran](https://www.linkedin.com/in/PatrickDoran)

---
